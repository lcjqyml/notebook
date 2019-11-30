1. 执行过大sql文件时需要设置：修改在 MySQL\MySQL Server 5.0\ 目录下面的my.ini文件[mysqld]下面加上以下配置 max_allowed_packet=106M
2. 创建新数据库
```sql
create database sms_tool charset=utf8;
```
3. 创建用户并授权
```sql
CREATE USER 'smstool'@'%' IDENTIFIED BY '!QAZ1qaz';
```
4. 授权用户
```mysql
GRANT ALL PRIVILEGES ON `sms_tool`.* TO 'smstool';
FLUSH PRIVILEGES;
```
