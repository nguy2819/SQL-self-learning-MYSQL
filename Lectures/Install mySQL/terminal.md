- After download the mySQP to macOS through the link: https://dev.mysql.com/downloads/mysql/ and choose macOS 10.13 (x86, 64-bit), DMG Archive to download

- In terminal, the root, like ~ borlandtien$, type:
```
echo 'export PATH=/usr/local/mysql/bin:$PATH' >> ~/.bash_profile
```
- Then type:
```
. ~/.bash_profile
```
- Later, type:
```
mysql
```
- If they appear: ERROR 1045 (28000): Access denied for user 'borlandtien'@'localhost' (using password: NO) => which means we already able to type mysql in terminal
- Then type:
```
mysql -u root -p
```
- After that, it will still ask you to enter the password. 
- After entered the password, it will appear: ERROR 1045 (28000): Access denied for user 'borlandtien'@'localhost' (using password: YES)
- It supposes to show up this - after you apply the password:
```
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.12 MySQL Community Server - GPL

Copyright (c) 2000, 2018, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

* If it didn't, type: "mysql -u root -p" and apply password again.

=> As long as, you type "mysql -u root -p" in the terminal, type your password, and it "Welcome to the MySQL monitor... mysql>" -> which means you are successfully login into mysql terminal.