```
SELECT @@time_zone, now();
SELECT @@global.time_zone, @@session.time_zone;
```

`/etc/my.cnf` or `/etc/mysql/conf.d/timezone.cnf`

```
[mysqld]
default-time-zone='+9:00'

