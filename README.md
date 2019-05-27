# sql-samples
A collection of SQL samples for PostgreSQL database.

### General commands
_connect_: `psql --host localhost --user postgres`  
_list databases_: `postgres=# \l`  
_connect to database_: `postgres=# \c pandi`  
_show schemas_: `pandi=# \dn`  
_set current schema_: `pandi=# SET search_path to gianluca;`  
_show current schema_: `pandi=# select current_schema();`  
_list all tables_: `pandi=# \dt`  
_describe a table_: `pandi=# \d tb_employee`  
