# https://phpstatic.com

PHP package able to install at linux or macOS.

linux CPU need support AVX,  kernel > 2.6.35

macOS need CPU >= haswell, os >= 10.14


# debian, ubuntu 

https://phpstatic.com/php-static-7.4_latest_amd64.deb

```sh
curl -O https://phpstatic.com/php-static-7.4_latest_amd64.deb
dpkg -i php-static-7.4_latest_amd64.deb
systemctl daemon-reload
systemctl enable php-fpm
systemctl start php-fpm
```
# redhat, centos 

https://phpstatic.com/php-static-7.4-latest.x86_64.rpm

# other linux

https://phpstatic.com/php-static-7.3.latest-linux.tar.xz

# macOS

https://phpstatic.com/php-static-7.3.latest-osx.tar.xz

# BSD & Windows

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
