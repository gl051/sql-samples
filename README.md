# sql-samples
A collection of SQL samples for PostgreSQL database.

### General commands
_connect_: `psql --host localhost --user postgres`  

### Database
_list databases_: `postgres=# \l`  
_connect to database_: `postgres=# \c pandi`  
_select database size_: `select pg_size_pretty(pg_database_size('my_db'));`

### Schema
_show schemas_: `pandi=# \dn`  
_set current schema_: `pandi=# SET search_path to gianluca;`  
_show current schema_: `pandi=# select current_schema();`  

### Table
_list all tables_: `pandi=# \dt`  
_describe a table_: `pandi=# \d tb_employee`

### JSON
_create table_: `create table tb_json(id integer primary key, description jsonb)`  
_insert json value_: `insert into tb_json values(3, '[{"name":"tommy", "score":90}, {"name":"Mark", "score":909}]');`  
```
testdb=# select * from tb_json where id = 3;
 id |                           description
----+------------------------------------------------------------------
  3 | [{"name": "tommy", "score": 90}, {"name": "Mark", "score": 909}]
(1 row)
```
_select indexed element in json value_: `select description->0 from tb_json where id = 3;`
```
testdb=# select description->0 from tb_json where id = 3;
            ?column?
--------------------------------
 {"name": "tommy", "score": 90}
(1 row)
```
