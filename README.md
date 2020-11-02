# Node.js_Mysql_8.0
Troubleshooting connection problems.

### Install the mysql driver.
https://www.npmjs.com/package/mysql

### The error!
From version 8 of mysql, when trying to make the connection, you will receive an error suggesting that mysql should be updated. The problem is actually that you will have to create a new user on mysql and give that new user the necessary permissions.

Example:
### In MySQL follow the steps: 

1st Create the user.

CREATE USER 'paulo'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';

2nd Give the permissions.

GRANT ALL PRIVILEGES ON * . * TO 'paulo'@'localhost';


Ready! Try to connect again and the problem will not occur again.
