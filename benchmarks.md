
test environment：debian10 amd64 E5-2650 v2 X2

test project: https://github.com/symfony/demo.git , with `env=prod`.

php-static vs php7.3-fpm(debian default package), `fpm.conf` and `php.ini` is same(except php-static-7.4 opcache.preload test).

php-static-7.4 with opcache.preload
```sh
 wrk -t8 -c200 -d10 http://pve/en/blog
Running 10s test @ http://pve/en/blog
  8 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    30.24ms    1.49ms  46.90ms   80.08%
    Req/Sec   829.29     28.55     0.93k    67.50%
  66075 requests in 10.01s, 35.73MB read
Requests/sec:   6601.60
Transfer/sec:      3.57MB
```

php-static-7.4:
```sh
wrk -t8 -c200 -d10 http://pve/en/blog
Running 10s test @ http://pve/en/blog
  8 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    34.54ms    1.49ms  53.78ms   77.15%
    Req/Sec   725.91     24.80   770.00     83.25%
  57861 requests in 10.02s, 31.29MB read
Requests/sec:   5776.89
Transfer/sec:      3.12MB
```

php-static-7.3:
```sh
wrk -t8 -c200 -d10 http://pve/en/blog
Running 10s test @ http://pve/en/blog
  8 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    34.41ms    1.47ms  55.48ms   77.89%
    Req/Sec   728.74     23.67   770.00     81.75%
  58075 requests in 10.01s, 31.40MB read
Requests/sec:   5799.65
Transfer/sec:      3.14MB
```

php7.3-fpm:
```sh
wrk -t8 -c200 -d10 http://pve:88/en/blog
Running 10s test @ http://pve:88/en/blog
  8 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    40.40ms    1.90ms  53.82ms   76.46%
    Req/Sec   620.36     33.44   720.00     70.25%
  49463 requests in 10.02s, 27.45MB read
Requests/sec:   4936.25
Transfer/sec:      2.74MB
```

fpm.conf
```conf
[www]
listen = 127.0.0.1:9000
listen.backlog = -1
listen.allowed_clients = 127.0.0.1
listen.owner = www-data
listen.group = www-data
listen.mode = 0666
security.limit_extensions = .php
user = www-data
group = www-data
pm = static
pm.max_children = 32
pm.max_requests = 1024
request_terminate_timeout = 100
request_slowlog_timeout = 3
slowlog = /var/log/php-slow.log
```

php.ini
```ini
max_execution_time = 10
max_input_time = 60
max_input_vars=4096
post_max_size=8M
upload_max_filesize=8M
expose_php=off
display_errors=0
display_startup_errors=1
opcache.enable = 1
;opcache.preload_user=www-data
;opcache.preload=/var/www/demo/var/cache/prod/App_KernelProdContainer.preload.php
```


nginx.conf
```conf
worker_processes  8;
events {
    worker_connections  1024;
}
http {
    include       mime.types;
    default_type  application/octet-stream;
    charset utf-8;
    sendfile on;
    sendfile_max_chunk 512k;
    tcp_nopush on;
    tcp_nodelay on;
    server_tokens off;
    keepalive_timeout 12s 12s;
    keepalive_requests 10240;
  server {
    listen 0.0.0.0:88 default;
    root /var/www/demo/public;
    server_name _;
    location / {
        try_files $uri /index.php$is_args$args;
    }
    location ~ ^/index\.php(/|$) {
        fastcgi_pass unix:/run/php/php7.3-fpm.sock;
        fastcgi_split_path_info ^(.+\.php)(/.*)$;
        include fastcgi.conf;
        fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
        fastcgi_param DOCUMENT_ROOT $realpath_root;
        internal;
    }
    location ~ \.php$ {
        return 404;
    }
  }
  server {
    listen 0.0.0.0:80;
    root /var/www/demo/public;
    server_name pve;
    location / {
        try_files $uri /index.php$is_args$args;
    }
    location ~ ^/index\.php(/|$) {
        fastcgi_pass php;
        fastcgi_split_path_info ^(.+\.php)(/.*)$;
        include fastcgi.conf;
        fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
        fastcgi_param DOCUMENT_ROOT $realpath_root;
        internal;
    }
    location ~ \.php$ {
        return 404;
    }
  }
}
```

sysctl.conf
```conf
net.core.rmem_max = 67108864
net.core.wmem_max = 67108864
net.core.rmem_default = 65536
net.core.wmem_default = 65536
net.core.netdev_max_backlog = 64436
net.core.somaxconn = 65536
net.ipv4.tcp_syncookies = 0
net.ipv4.tcp_tw_reuse = 1
net.ipv4.tcp_fin_timeout = 30
net.ipv4.tcp_keepalive_time = 1200
net.ipv4.ip_local_port_range = 10000 65000
net.ipv4.tcp_max_syn_backlog = 32768
net.ipv4.tcp_max_tw_buckets = 72768
net.ipv4.tcp_fastopen = 3
net.ipv4.tcp_rmem = 32768 87380 67108864
net.ipv4.tcp_wmem = 32768 65536 67108864
net.ipv4.tcp_mtu_probing = 1
net.ipv4.ip_local_port_range = 40000    65000
```
