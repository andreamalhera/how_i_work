# Starting any database
* Start hdfs server if necessary
* Start database server
* Start client

## Mongo
### How to connect to Mongo
* `mongo localhost:<27016>/<review_widgets> --authenticationDatabase admin  -u <widgets-ro> --password <pwd>`
* `use <collection>`
* `db.<collection>.findOne()`

## PSQL
### How to access the psql databases from a host-server

* Login into the server: `ssh <username>@<host-server>.<domain.com>`
* To use psql from the commandline: 
      `psql -h <host-server>.<domain.com> -U <user> -d <database> -c "<SQL-command>"`
* Some useful psql commands for after `-c`:
     * To list databases `SELECT datname FROM pg_database;`
     * To list all tables `SELECT * FROM pg_catalog.pg_tables;`
   
### Save to file 
`"COPY (SELECT column_1,column_2,column_3 FROM <collection>.<table> WHERE <column> = '<value>') TO STDOUT" >> file_name`

### How to look into db using pgadmin
* in the terminal: `pgadmin4`
* view data (right-click) on table (not schema)
