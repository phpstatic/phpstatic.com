# https://phpstatic.com

PHP package able to install at linux or macOS.

linux package need  CPU support AVX,  kernel >= 2.6.35

macOS package need CPU >= haswell, os >= 10.14


# debian, ubuntu 

* https://phpstatic.com/php-static-7.4_latest_amd64.deb
* https://phpstatic.com/php-static-7.3_latest_amd64.deb
* https://phpstatic.com/php-static-7.2_latest_amd64.deb

```sh
curl -O https://phpstatic.com/php-static-7.4_latest_amd64.deb
dpkg -i php-static-7.4_latest_amd64.deb
/etc/init.d/php-fpm status
```
# redhat, centos 

* https://phpstatic.com/php-static-7.4-latest.x86_64.rpm
* https://phpstatic.com/php-static-7.3-latest.x86_64.rpm
* https://phpstatic.com/php-static-7.2-latest.x86_64.rpm


```sh
curl -O https://phpstatic.com/php-static-7.4-latest.x86_64.rpm
rpm -i php-static-7.4-latest.x86_64.rpm
systemctl daemon-reload
systemctl enable php-fpm
systemctl start php-fpm
```

# other linux

* https://phpstatic.com/php-static-7.4.latest-linux.tar.xz
* https://phpstatic.com/php-static-7.3.latest-linux.tar.xz
* https://phpstatic.com/php-static-7.2.latest-linux.tar.xz


```sh
curl -O https://phpstatic.com/php-static-7.4.latest-linux.tar.xz
tar xvf php-static-7.4.latest-linux.tar.xz -C /
systemctl daemon-reload
systemctl enable php-fpm
systemctl start php-fpm
```


# macOS

* https://phpstatic.com/php-static-7.4.latest-osx.tar.xz
* https://phpstatic.com/php-static-7.3.latest-osx.tar.xz
* https://phpstatic.com/php-static-7.2.latest-osx.tar.xz

```sh
curl -O https://phpstatic.com/php-static-7.4.latest-osx.tar.xz
tar xvf php-static-7.4.latest-osx.tar.xz -C /
```


# BSD

not ready yet

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
redis
Reflection
session
shmop
SimpleXML
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
tidy
tokenizer
xlswriter
xml
xmlreader
xmlwriter
yaml
zip
zlib
zstd

[Zend Modules]
Zend OPcache
```
