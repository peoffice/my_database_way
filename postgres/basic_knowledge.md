#### postgresql 11
###### Load Sample Data
* [Download DVD rental data](http://www.postgresqltutorial.com/postgresql-sample-database/)
* [Load data based on postgresql](http://www.postgresqltutorial.com/load-postgresql-sample-database/)
##### 数据类型
###### 数值类型
* smallint
* integer
* bigint
* decimal
* numeric
* real
* double
* serial
* bigserial
###### 字符串类型
* char(size)
* character(size)
* varchar(size)
* character varying(size)
* text
###### 日期/时间类型
* timestamp[(p)][不带时区]
* timestamp[(p)]带时区
* date
* time[(p)][不带时区]
* time[(p)]带时区
* interval[fields][(p)]
###### 其他
* boolean
* money
* 几何类型
  * point
  * line
  * lseg
  * box
  * path
  * polygon
  * circle
##### Commands
* 启动数据库
  > ```pg_ctl -D /xx/pgdata start```
* 产看版本
  > ```pg_ctl --version```
* 命令行登陆数据库
  > ```psql -U username -d dbname -h hostip -p port```
* 列出所有数据库
  > ```\l```
* 切换数据库
  > ```\c dbname```
* 列出当前数据库的所有表
  > ```\d```
* 查看指定表的所有字段
  > ```\d tablename```
* 查看指定表的基本情况
  > ```\d+ tablename```
* 推出操作
  > ```q```
* 新建表
  > ```create table TESTCASE(id INTEGER, task_class INTEGER,age TEXT,PRIMARY KEY(id, task_class));```
  > ```create table CREATETASK_CHKID_N( id SERIAL PRIMARY KEY, chk_id TEXT, n INTEGER);```
* 删除表
  > ```drop table REL_CROSS_NODE;```
* 清空表
  > ```delete from [表名];```
* 添加字段
  > ```alter table [表名] add column [字段名] [类型];```
* 更改字段
  > ```alter table [表名] rename column [旧字段名] to [新字段名];```
* 删除字段
  > ```alter table [表名] drop column [字段名];```
* 在表中插入一行数据
  > ```insert into assist_info(id,maat_id,block_type) values('F006','F7775',1);```
* 表中删除一行数据
  > ```delete from [表名] where [该行特征];```
* 修改表中数据
  > ```update [表名] set [目标字段名]=[目标值] where [该行特征];```
* 删除表
  > ```drop table [表名];```
#### 参考
* [postgresql docs](https://www.postgresql.org/docs/)