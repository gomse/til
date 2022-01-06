```
SHOW DATABASES;
```

```
CREATE DATABASE dbname;
```

```
USE mysql;

SELECT host,user,password FROM USER;

CREATE USER 'username'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON dbname.* TO 'username'@'%';

FLUSH PRIVILEGES;
```

