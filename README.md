# flyway-migration
flyway migration to production db schema updates

# Naming
In order to be picked up by Flyway, SQL migrations must comply with the following naming pattern:

## Versioned Migrations

- < Prefix >< Version >__< description_of_the_file >< suffix >

ex:
 - V2__Add_new_table.sql
 - U2__Add_new_table.sql
 - R__Add_new_table.sql

### Details

- Prefix: V for versioned (configurable), U for undo (configurable) and R for repeatable migrations (configurable)
- Version: Version with dots or underscores separate as many parts as you like (Not for repeatable migrations)
- Separator: __ (two underscores) (configurable)
- Description: Underscores or spaces separate the words
- Suffix: .sql (configurable)
