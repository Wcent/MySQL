# MySQL</br>
commands about mysql</br>
</br>
MySQL命令总结</br>
</br>
连接方式</br>
MySQL -h hostname -u root -p</br>
MySQL -u root -p</br>
MySQL -hlocalhost -uroot -pxxx</br>
MySQL -uroot -pxxx</br>
</br>
退出</br>
quit</br>
exit</br>
</br>
查看数据库信息</br>
show databases;</br>
</br>
创建数据库</br>
create database db_name;</br>
</br>
删除数据库</br>
drop database [if exists] db_name;</br>
</br>
使用某个数据库</br>
use database;</br>
</br>
查看表信息</br>
show tables;</br>
</br>
查看表结构</br>
desc table;</br>
</br>
创建表</br>
create table t_name (</br>
col_1 col_type [完整性约束],</br>
col_2 col_type [完整性约束],</br>
col_3 col_type [完整性约束],</br>
...</br>
col_n col_type [完整性约束]</br>
);</br>
</br>
常用完整性约束</br>
PRIMARY KEY：主键</br>
UNIQUE：唯一性</br>
NOT NULL：非空值</br>
AUTO INCREMENT：整数默认自增1</br>
UNSIGNED：无符号整数</br>
DEFAULT defualt_value：默认值</br>
DEFAULT cur_timestamp：新增操作取值当前时间（仅用于timestamp数据列）</br>
ON UPDATE cur_timestamp：修改操作取值当前时间（仅用于timestamp数据列）</br>
CHARACTER SET name：指定字符集（仅用于字符串列）</br>
</br>
删除表</br>
drop table [if exists] t_name [, t2_name]...;</br>
</br>
修改表结构</br>
alter table t_name action;</br>
action为具体操作语句</br>
</br>
</br>
插入操作</br>
insert into t_name [(col_1, col_2, col_3, ..., col_n)] values(val_1, val_2, val_3, ..., val_n);</br>
</br>
从表选择插入（插入多条）</br>
insert into t_name[(col_1, col_2, col_3, ..., col_n)] select c1, c2, c3, ..., cn from t2_name [where condition];</br>
</br>
更新操作</br>
update t_name set col_1=val_1, col_2=val_2, col_3=val_3, ..., col_n=val_n [where condition];</br>
</br>
删除操作</br>
delete from t_name [where condition];</br>
</br>
