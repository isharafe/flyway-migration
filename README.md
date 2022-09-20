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


## Note
 - check the db version and the flyway version
 - https://stackoverflow.com/questions/70438180/what-is-the-last-version-of-flyway-community-edition-that-supported-mysql-5-7

Flyway Community Edition 8.0.0-beta1 dropped support for databases older than 5 years, including MySQL 5.7.
The minimum supported version of MySQL was increased from 5.7 to 8.0 in this commit, which was introduced in Flyway 8.0.0-beta1.
Currently, the latest community edition version that supports MySQL 5.7 is Flyway 7.15.0.
