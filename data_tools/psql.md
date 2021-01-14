# PSQL
## How to access the psql databases from a host-server

* Login into the server: `ssh <username>@<host-server>.<domain.com>`
* To use psql from the commandline: 
      `psql -h <host-server>.<domain.com> -U <user> -d <database> -c "<SQL-command>"`
* Some useful psql commands for after `-c`:
     * To list databases "SELECT datname FROM pg_database;"
     * To list all tables "SELECT * FROM pg_catalog.pg_tables;"
   