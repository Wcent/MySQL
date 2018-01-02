# MySQL
commands about mysql

MySQL命令总结

连接方式
MySQL -h hostname -u root -p
MySQL -u root -p
MySQL -hlocalhost -uroot -pxxx
MySQL -uroot -pxxx

退出
quit
exit

查看数据库信息
show databases;

创建数据库
create database db_name;

删除数据库
drop database [if exists] db_name;

使用某个数据库
use database;

查看表信息
show tables;

查看表结构
desc table;

创建表
create table t_name (
col_1 col_type [完整性约束],
col_2 col_type [完整性约束],
col_3 col_type [完整性约束],
...
col_n col_type [完整性约束]
);

常用完整性约束
PRIMARY KEY：主键
UNIQUE：唯一性
NOT NULL：非空值
AUTO INCREMENT：整数默认自增1
UNSIGNED：无符号整数
DEFAULT defualt_value：默认值
DEFAULT cur_timestamp：新增操作取值当前时间（仅用于timestamp数据列）
ON UPDATE cur_timestamp：修改操作取值当前时间（仅用于timestamp数据列）
CHARACTER SET name：指定字符集（仅用于字符串列）

删除表
drop table [if exists] t_name [, t2_name]...;

修改表结构
alter table t_name action;
action为具体操作语句


插入操作
insert into t_name [(col_1, col_2, col_3, ..., col_n)] values(val_1, val_2, val_3, ..., val_n);

从表选择插入（插入多条）
insert into t_name[(col_1, col_2, col_3, ..., col_n)] select c1, c2, c3, ..., cn from t2_name [where condition];

更新操作
update t_name set col_1=val_1, col_2=val_2, col_3=val_3, ..., col_n=val_n [where condition];

删除操作
delete from t_name [where condition];
