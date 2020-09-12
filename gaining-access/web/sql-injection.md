# SQL Injection

A nice way to check for this vulnerability is to input a quote and see if something goes wrong.

SQL injection can be used to bypass login, but it can also be used to gather information. Of the things you can discover:

* The data itself.
* Enumerate other tables.
* Amount of rows and columns.
* The version of the DB.
* The user that runs the queries

## Notes

Some DBs are configured to be able to interact with the OS! You can load and write to files.

The code may expect one query, so when injecting queries a LIMIT can be added.  


