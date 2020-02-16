
test environment：debian10 amd64 E5-2650 v2 X2

test project: https://github.com/symfony/demo.git , with `env=prod`.

php-static-7.3 vs php7.3-fpm(debian default package), `fpm.conf` and `php.ini` is same.


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

