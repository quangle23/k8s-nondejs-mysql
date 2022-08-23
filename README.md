# NodeJS and MySQL on Kubernetes

## MySQL considerations

Create a user for your database with `'dbuser'@'%'` with general scope as you can't guarantee what interal IP you will be connecting from.

```
CREATE DATABASE dbname;
CREATE USER 'dbuser'@'%' IDENTIFIED BY 'TODO_password';
GRANT ALL PRIVILEGES ON dbname.* TO 'dbuser'@'%';
FLUSH PRIVILEGES;
```
