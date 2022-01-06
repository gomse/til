## Docker에 MariaDB 설치

## install

```sh
docker pull mariadb
docker container run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=1234 -v /Users/Shared/data/mariadb:/var/lib/mysql --name mariadb mariadb
docker exec -i -t mariadb bash
```

```sh
mysql -uroot -p1234
show databases;
```

## utf-8 설정

```sh
apt-get update
apt-get install vim
```

```sh
cd /etc/mysql/conf.d
vi charset.cnf
```

```
[mysqld]
collation-server=utf8_unicode_ci
init-connect='SET NAMES utf8'
character_set_server=utf8

[client]
default-character-set=utf8

[mysqldump]
default-character-set=utf8

[mysql]
default-character-set=utf8
```

## 재시작

```sh
docker stop mariadb
docker start mariadb
```

```sh
docker exec -i -t mariadb bash
mysql -uroot -p1234
show variables like 'c%';
```

## logs

```sh
docker logs -f --tail=10 mariadb
```

