# Spanner & wrench & spanner-cli by docker-compose

## Requirements:
* docker >= 19.03.0+
* docker-compose >= 1.27.0+

## Quick Start
* Clone or download this repository
* Go inside of directory,  `cd compoose-spanner`
* Run this command `docker-compose up -d`

## Environments
This Compose file contains the following environment variables:

* `PROJECT_ID` the default value is **test-project**
* `INSTANCE_NAME` the default value is **test-instance**
* `DATABASE_NAME` the default value is **test-database**

## Access to spanner:
* `SPANNER_EMULATOR_HOST=localhost:9010`

## Access to spanner with spanner-cli:

* Run this command `docker-compose exec spanner-cli spanner-cli -p test-project -i test-instance -d test-database`
    * **project:** test-project (as a default)
    * **instance:** test-instance (as a default)
    * **database:** test-database (as a default)

```
$ docker-compose exec spanner-cli spanner-cli -p test-project -i test-instance -d test-database
Connected.
spanner>
      -> show tables;
+-------------------------+
| Tables_in_test-database |
+-------------------------+
| Singers                 |
| Albums                  |
+-------------------------+
2 rows in set (0.01 sec)
```
