# test-dbs-compose

## sqlite

- Copy the sqlite3 database file to the `dbfiles/` directory

- Run docker compose

  ```console
  docker compose up
  ```

- In the adminer web UI (Http://localhost:8080)
  - System: `SQLite 3`
  - Username: `<leave blank>`
  - Password: `adminer` (specified in ADMINER_PASSWORD)
  - Database: `/dbfiles/<file_name_here>`

## mysql

- Run docker compose with `--profile mysql` option (to start a mysql
  container in addition to adminer)

  ```console
  docker compose --profile mysql up
  ```

- In the adminer web UI (Http://localhost:8080)
  - System: `MySQL`
  - Server: `mysql` (container name)
  - Username: `root`
  - Password: `mysql` (specified in  MYSQL_ROOT_PASSWORD)
  - Database: `<leave blank to show all dbs>`

- A dump can be imported using the "Import" link
