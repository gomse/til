[mysql]

```sh
sudo apt purge mysql-server
sudo apt purge mysql-common
```

[mariadb]

```sh
sudo apt purge mariadb-server
sudo apt purge mariadb-common
```

[common]

```sh
sudo rm -rf /var/log/mysql
sudo rm -rf /var/log/mysql.*
sudo rm -rf /var/lib/mysql
sudo rm -rf /etc/mysql
```

