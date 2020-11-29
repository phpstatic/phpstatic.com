# [https://phpstatic.com](https://phpstatic.com/phpinfo.html)

PHPStatic package is build for better performance, check our [benchmarks](https://github.com/phpstatic/phpstatic.com/blob/master/benchmarks.md).

PHPStatic package is build as static shared object, to reduce the dynamic library runtime overheads and attack surface. Static link also allow our package suite for most of linux distribution, avoid dependent library miss match problem during system upgrade time. 
```sh
$ file /usr/local/bin/php
/usr/local/bin/php: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, stripped

$ readelf -l ./php

Elf file type is DYN (Shared object file)
Entry point 0x37f9a8
There are 7 program headers, starting at offset 64

Program Headers:
  Type           Offset             VirtAddr           PhysAddr
                 FileSiz            MemSiz              Flags  Align
  LOAD           0x0000000000000000 0x0000000000000000 0x0000000000000000
                 0x0000000002b48980 0x0000000002b48980  R E    0x200000
  LOAD           0x0000000002b49920 0x0000000002d49920 0x0000000002d49920
                 0x0000000000256b80 0x000000000035ee48  RW     0x200000
  DYNAMIC        0x0000000002d45540 0x0000000002f45540 0x0000000002f45540
                 0x00000000000001d0 0x00000000000001d0  RW     0x8
  TLS            0x0000000002b49920 0x0000000002d49920 0x0000000002d49920
                 0x0000000000000088 0x0000000000005d98  R      0x20
  GNU_EH_FRAME   0x000000000278ccbc 0x000000000278ccbc 0x000000000278ccbc
                 0x0000000000080d5c 0x0000000000080d5c  R      0x4
  GNU_STACK      0x0000000000000000 0x0000000000000000 0x0000000000000000
                 0x0000000000000000 0x0000000000000000  RW     0x10
  GNU_RELRO      0x0000000002b49920 0x0000000002d49920 0x0000000002d49920
                 0x00000000001fd6e0 0x00000000001fd6e0  R      0x1

 Section to Segment mapping:
  Segment Sections...
   00     .hash .gnu.hash .dynsym .dynstr .gnu.version .gnu.version_d .rela.dyn .init .plt .text .fini .rodata .eh_frame_hdr .eh_frame .gcc_except_table 
   01     .tdata .init_array .fini_array .ctors .dtors .data.rel.ro .dynamic .got .data .bss 
   02     .dynamic 
   03     .tdata .tbss 
   04     .eh_frame_hdr 
   05     
   06     .tdata .init_array .fini_array .ctors .dtors .data.rel.ro .dynamic .got 
```


PHPStatic package also build for security,  by add gcc flags `-fstack-clash-protection`, `-fstack-protector-strong`, `-Wp,-D_FORTIFY_SOURCE=2`, `-Wp,-D_GLIBCXX_ASSERTIONS`, `-fPIE`, `-Wl,-z,now`, `-Wl,-z,relro`, `-Wl,-z,text`, `-Wl,-z,noexecstack` to enable `Address space layout randomization`, `Full RELRO`, `STACK CANARY`, `non-executable stack`, `FORTIFY`, `stack clash protection`, `stack overflow protection`.

PHPStatic is immune to LD_PRELOAD preload attacks like [this](https://github.com/yangyangwithgnu/bypass_disablefunc_via_LD_PRELOAD).

Linux package need CPU support AVX.

[macOS package](https://phpstatic.com/macOS/) need CPU >= Sandy Bridge(2011), os >= 10.13(High Sierra), [macOS package](https://phpstatic.com/macOS/) also work for VM with Penryn(+aes, +avx) CPU.

[maxOS >= 10.9 Mavericks](https://phpstatic.com/osx109/) package is not support any more, you can download [old MAC OSX packages](https://phpstatic.com/osx109/) for develop only.

# [docker](https://hub.docker.com/r/phpstatic/php)

run this on your project dirs:

```sh
docker pull phpstatic/php:7.4.13
docker run --name php74 -itd -v $(pwd):/app --mount source=php74_etc,target=/usr/local/etc/php phpstatic/php:7.4.13
docker logs php74
docker volume inspect php74_etc
docker exec -i -t php74 composer install
docker exec -i -t php74 ash
```

# debian, ubuntu 

* https://phpstatic.com/php-static-8.0-latest-amd64.deb
* https://phpstatic.com/php-static-7.4-latest-amd64.deb
* https://phpstatic.com/php-static-7.3-latest-amd64.deb
* https://phpstatic.com/php-static-7.2-latest-amd64.deb
* https://phpstatic.com/nginx-static-latest-amd64.deb

this work with systemd,  for old debian/ubuntu please try docker or https://phpstatic.com/linux/

```sh
echo deb http://phpstatic.com/debian/ / > /etc/apt/sources.list.d/phpstatic.list
apt-get install gnupg curl sudo
curl -L https://phpstatic.com/repo.gpg | sudo apt-key add -
apt-get update
apt-get install php-static-7.4 nginx-static
/etc/init.d/php-fpm status
```
# CentOS/Fedora/Red Hat/SUSE

* https://phpstatic.com/php-static-8.0-latest-x86_64.rpm
* https://phpstatic.com/php-static-7.4-latest-x86_64.rpm
* https://phpstatic.com/php-static-7.3-latest.x86_64.rpm
* https://phpstatic.com/php-static-7.2-latest.x86_64.rpm
* https://phpstatic.com/nginx-static-latest-x86_64.rpm


this work with systemd,  for old redhat/centos please try docker or https://phpstatic.com/linux/

```sh
curl -L https://phpstatic.com/centos/phpstatic.repo -o /etc/yum.repos.d/phpstatic.repo
yum update
yum install php-static-7.4 nginx-static -y 
systemctl status php-fpm
```

# alpine 

* https://phpstatic.com/php-static-8.0-latest-x86_64.apk
* https://phpstatic.com/php-static-7.4-latest-x86_64.apk
* https://phpstatic.com/php-static-7.3-latest-x86_64.apk
* https://phpstatic.com/php-static-7.2-latest-x86_64.apk
* https://phpstatic.com/nginx-static-latest-x86_64.apk

```sh
curl -o /etc/apk/keys/phpstatic.com-5e2a99b5.rsa.pub -L https://phpstatic.com/alpine/phpstatic.com-5e2a99b5.rsa.pub
echo http://phpstatic.com/alpine >> /etc/apk/repositories
apk update
apk add php-static-7.4 nginx-static 
/etc/init.d/php-fpm status
```

# others linux

* https://phpstatic.com/php-static-8.0-latest-linux-x64.tar.gz
* https://phpstatic.com/php-static-7.4-latest-linux-x64.tar.gz
* https://phpstatic.com/php-static-7.3-latest-linux-x64.tar.gz
* https://phpstatic.com/php-static-7.2-latest-linux-x64.tar.gz
* https://phpstatic.com/nginx-static-latest-linux-x64.tar.gz


```sh
curl -O https://phpstatic.com/php-static-7.4-latest-linux-x64.tar.gz
curl -O https://phpstatic.com/nginx-static-latest-linux-x64.tar.gz
tar xvf php-static-* -C /
tar xvf nginx-static-* -C /

/usr/local/bin/php-fpm
killall php-fpm

/usr/sbin/nginx
/usr/sbin/nginx -s stop
```


# macOS

* https://phpstatic.com/php-static-8.0-latest-osx-x64.tar.gz
* https://phpstatic.com/php-static-7.4-latest-osx-x64.tar.gz
* https://phpstatic.com/php-static-7.3-latest-osx-x64.tar.gz
* https://phpstatic.com/php-static-7.2-latest-osx-x64.tar.gz

```sh
curl -O https://phpstatic.com/php-static-7.4-latest-osx-x64.tar.gz
tar xvf php-static-* -C /
otool -L /usr/local/bin/php
/usr/local/bin/php:
	/usr/lib/libresolv.9.dylib (compatibility version 1.0.0, current version 1.0.0)
	/System/Library/Frameworks/CoreFoundation.framework/Versions/A/CoreFoundation (compatibility version 150.0.0, current version 1455.12.0)
	/usr/lib/libSystem.B.dylib (compatibility version 1.0.0, current version 1252.50.4)
```

# Windows 

try docker or https://docs.microsoft.com/en-us/windows/wsl/install-win10 


# BSD

not ready yet, try docker 

# [xdebug](https://github.com/xdebug/xdebug), [tideways_xhprof](https://github.com/tideways/php-xhprof-extension.git), [SPX](https://github.com/NoiseByNorthwest/php-spx.git), [SeasLog](https://github.com/SeasX/SeasLog), [wasm](https://github.com/wasmerio/php-ext-wasm), [taint](https://github.com/laruence/taint), [ast](https://github.com/nikic/php-ast), [componere](https://github.com/krakjoe/componere)

`xdebug`, `taint`, `tideways_xhprof`, `SPX`, `SeasLog`, `wasm`, `ast`, `componere`, `xattr` is default disabled, to enable it add `disable_extensions=none` into `php.ini`.

`xdebug` conflict with `taint`, remember just enable one of them.

# [php -m](https://phpstatic.com/phpinfo.html)
```ini
[PHP Modules]
amqp
apcu
ast
base58
bcmath
brotli
bz2
calendar
componere
Core
ctype
curl
date
dom
event
exif
fileinfo
filter
ftp
gd
gmp
grpc
hash
hoedown
iconv
igbinary
imap
intl
ip2region
jsmin
json
json_post
jwt
libxml
lz4
mbstring
memcached
mongodb
msgpack
mysqli
mysqlnd
OAuth
openssl
pcntl
pcre
PDO
pdo_mysql
pdo_pgsql
pdo_sqlite
pgsql
phalcon
Phar
posix
protobuf
pspell
psr
rar
rdkafka
readline
redis
Reflection
sass
SeasLog
session
shmop
SimpleXML
snappy
soap
sockets
sodium
solr
SPL
SPX
sqlite3
standard
swoole
swoole_orm
sysvmsg
sysvsem
sysvshm
taint
thrift_protocol
tideways_xhprof
tidy
tokenizer
trie_filter
wasm
xattr
xdebug
xlswriter
xml
xmlreader
xmlwriter
xsl
yaconf
yaml
yar
Zend OPcache
zip
zlib
zmq
zstd

[Zend Modules]
Xdebug
Zend OPcache

```

# nginx -V

nginx 1.18.0 is build with [http3](https://en.wikipedia.org/wiki/HTTP/3), [njs](https://github.com/nginx/njs.git)(0.4.3), [io_uring](https://github.com/hakasenyang/openssl-patch/pull/41), ssl_stapling+BoringSSL support(the only solution that support multi domain without cronjob). 

nginx-uring require kernel >= 5.1.

```sh
nginx version: nginx/1.18.0 (nginx)
built by gcc version 9.3.0
built with OpenSSL 1.1.0 (compatible; BoringSSL) (running with BoringSSL)
TLS SNI support enabled
configure arguments:--conf-path=/etc/nginx/nginx.conf --pid-path=/var/run/nginx.pid --lock-path=/var/lock/nginx.lock --user=www-data --group=www-data --without-select_module --with-poll_module --with-file-aio --with-threads --with-http_ssl_module --with-http_v2_module --with-http_realip_module --with-http_sub_module --with-http_stub_status_module --with-http_geoip_module --with-http_slice_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_auth_request_module --with-http_secure_link_module --with-stream --with-stream_ssl_module --with-stream_geoip_module --with-stream_ssl_preread_module --with-stream_realip_module --with-pcre --with-pcre-jit --with-openssl --with-zlib --with-zlib-asm=pentiumpro --with-libatomic --with-http_addition_module --without-http_uwsgi_module --with-mail --with-mail_ssl_module --with-http_mp4_module --with-http_flv_module --add-module=devel_kit --add-module=brotli --add-module=zstd --add-module=substitutions_filter --add-module=headers-more --add-module=h264_streaming --add-module=vod --add-module=flv --add-module=dynamic_limit_req --add-module=slice --add-module=njs/nginx --add-module=vts --add-module=websockify --with-http_v3_module --with-openssl --with-quiche
```
