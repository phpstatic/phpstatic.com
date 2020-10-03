phpstatic for linux package support apparmor_hat to protected your server, to enable it add `apparmor_hat = your_hat_name` into your php-fpm pool.

`/etc/apparmor.d/usr.local.sbin.php-fpm` example:
```conf
#include <tunables/global>
profile php-fpm /usr/local/sbin/php-fpm flags=(attach_disconnected) {
  #include <abstractions/base>
  #include <abstractions/nameservice>

  capability net_admin,
  capability setuid,
  capability setgid,
  capability chown,
  capability kill,

  /usr/local/etc/php/ r,
  /usr/local/etc/php/** r,

  /proc/loadavg r,
  /proc/@{pid}/attr/current rw,
  /dev/shm/mongoc-* rw,

  /var/lock/php-fpm.lock rw,
  /var/log/php-fpm.log rw,
  /var/log/php-slow.log rw,
  /var/log/php/* rw,

  /run/php-fpm/fpm-*.socket rwlk,
  /run/php-fpm/php-fpm.pid rwlk,
  /run/php-fpm.pid rwlk,

  /opt/web/** rk,

  # Zend opcache
  /tmp/.ZendSem.* rwlk,
  /tmp/php* rw,

  deny / rw,

  signal (send) peer=php-fpm//*,

  change_profile -> php-fpm//*,

}
```
