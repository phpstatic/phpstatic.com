# https://phpstatic.com

PHP package able to install at any linux distribution version.

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
