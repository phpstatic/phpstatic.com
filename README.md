# https://phpstatic.com

PHP package able to install at linux or macOS.

linux package need  CPU support AVX,  kernel >= 4.4.10

macOS package need CPU >= haswell, os >= 10.14


# debian, ubuntu 

* https://phpstatic.com/php-static-7.4-latest-amd64.deb
* https://phpstatic.com/php-static-7.3-latest-amd64.deb
* https://phpstatic.com/php-static-7.2-latest-amd64.deb
* https://phpstatic.com/nginx-static-latest-amd64.deb

this work with systemd,  for old debian/ubuntu please try https://phpstatic.com/linux/

```sh
echo deb https://phpstatic.com/debian/ / > /etc/apt/sources.list.d/phpstatic.list
curl -L https://phpstatic.com/repo.gpg | sudo apt-key add -
apt-get update
apt-get install php-static-7.4 nginx-static
/etc/init.d/php-fpm status
```
# redhat, centos >=7

* https://phpstatic.com/php-static-7.4-latest-x86_64.rpm
* https://phpstatic.com/php-static-7.3-latest.x86_64.rpm
* https://phpstatic.com/php-static-7.2-latest.x86_64.rpm
* https://phpstatic.com/nginx-static-latest-x86_64.rpm


this work with systemd,  for old redhat/centos please try https://phpstatic.com/linux/

```sh
curl -L https://phpstatic.com/centos/phpstatic.repo -o /etc/yum.repos.d/phpstatic.repo
yum update
yum install php-static-7.4 nginx-static -y 
systemctl status php-fpm
```

# alpine 


* https://phpstatic.com/php-static-7.4-latest-x86_64.apk
* https://phpstatic.com/php-static-7.3-latest-x86_64.apk
* https://phpstatic.com/php-static-7.2-latest-x86_64.apk
* https://phpstatic.com/nginx-static-latest-x86_64.apk

```sh
curl -o /etc/apk/keys/phpstatic.com-5e2a99b5.rsa.pub -L https://phpstatic.com/alpine/phpstatic.com-5e2a99b5.rsa.pub
echo https://phpstatic.com/alpine >> /etc/apk/repositories
apk update
apk add php-static-7.4 nginx-static 
/etc/init.d/php-fpm status
```

# others linux

* https://phpstatic.com/php-static-7.4-latest-linux-x64.tar.xz
* https://phpstatic.com/php-static-7.3-latest-linux-x64.tar.xz
* https://phpstatic.com/php-static-7.2-latest-linux-x64.tar.xz
* https://phpstatic.com/nginx-static-latest-linux-x64.tar.xz


```sh
curl -O https://phpstatic.com/php-static-7.4-latest-linux-x64.tar.xz
tar xvf nginx-static-* -C /

/usr/local/bin/php-fpm
killall php-fpm

/usr/sbin/nginx
/usr/sbin/nginx -s stop
```


# macOS

* https://phpstatic.com/php-static-7.4-latest-osx-x64.tar.xz
* https://phpstatic.com/php-static-7.3-latest-osx-x64.tar.xz
* https://phpstatic.com/php-static-7.2-latest-osx-x64.tar.xz

```sh
curl -O https://phpstatic.com/php-static-7.4-latest-osx-x64.tar.xz
tar xvf php-static-* -C /
```

# Windows 

try https://docs.microsoft.com/en-us/windows/wsl/install-win10 


# BSD

not ready yet

# xdebug, tideways_xhprof

`xdebug` and `tideways_xhprof` is default disabled, to enable it add `disable_extensions=none` into `php.ini`.

# php -m
```ini
[PHP Modules]
apcu
bcmath
brotli
bz2
calendar
Core
ctype
curl
date
dom
exif
fileinfo
filter
ftp
gd
gmp
hash
iconv
igbinary
intl
json
jwt
libxml
mbstring
memcached
mongodb
msgpack
mysqli
mysqlnd
openssl
pcre
PDO
pdo_mysql
pdo_pgsql
pdo_sqlite
pgsql
Phar
posix
protobuf
psr
rdkafka
redis
Reflection
session
shmop
SimpleXML
snappy
soap
sockets
sodium
SPL
sqlite3
standard
swoole
swoole_orm
sysvmsg
sysvsem
sysvshm
tideways_xhprof
tidy
tokenizer
xdebug
xlswriter
xml
xmlreader
xmlwriter
yaml
Zend OPcache
zip
zlib
zstd

[Zend Modules]
Xdebug
Zend OPcache
```

# nginx -V

```sh
nginx version: nginx/1.17.8 (nginx)
built by gcc version 9.2.0
built with OpenSSL 1.1.1d  10 Sep 2019
TLS SNI support enabled
configure arguments:--conf-path=/etc/nginx/nginx.conf --pid-path=/var/run/nginx.pid --lock-path=/var/lock/nginx.lock --user=www-data --group=www-data --without-select_module --with-poll_module --with-file-aio --with-threads --with-http_ssl_module --with-http_v2_module --with-http_realip_module --with-http_sub_module --with-http_stub_status_module --with-http_geoip_module --with-http_slice_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_auth_request_module --with-http_secure_link_module --with-stream --with-stream_ssl_module --with-stream_geoip_module --with-stream_ssl_preread_module --with-stream_realip_module --with-pcre --with-pcre-jit --with-openssl --with-zlib --with-zlib-asm=pentiumpro --with-libatomic --with-http_addition_module --without-http_uwsgi_module --with-mail --with-mail_ssl_module --with-http_mp4_module --with-http_flv_module --add-module=devel_kit --add-module=dav --with-http_dav_module --add-module=brotli --add-module=zstd --add-module=substitutions_filter --add-module=headers-more --add-module=h264_streaming --add-module=vod --add-module=flv --add-module=upload --add-module=dynamic_limit_req --add-module=slice --add-module=njs/nginx --add-module=vts --add-module=websockify
```
