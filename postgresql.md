# PostgreSQL

## Install on Ubuntu 18.04 / 19.10

* PostgreSQL 11

    ```bash
    sudo apt update
    sudo apt install postgresql-client postgresql-11
    ```

## Config PostgreSQL

```bash
sudo -u postgres psql
```

The above command gets you the psql command line interface in full admin mode

### Create User

```bash
postgres=# CREATE USER myuser WITH ENCRYPTED PASSWORD 'mypass';
```

### Create DataBase

```bash
postgres=# CREATE DATABASE yourdbname;
postgres=# GRANT ALL PRIVILEGES ON DATABASE yourdbname TO youruser;
```

### Altering Existing User Permissions

```bash
postgres=# ALTER USER youruser WITH OPTION1 OPTION2 OPTION3;
```

* Assigning SUPERUSER Permission

    ```bash
    postgres=# ALTER USER youruser WITH SUPERUSER;
    ```

* Revoking SUPERUSER Permissions

    ```bash
    postgres=# ALTER USER youruser WITH NOSUPERUSER;
    ```

### Utils

* List all the existing users

    ```bash
    postgres=# SELECT usename FROM pg_user;
    ```

* Viewing Existing User Permissions

    ```bash
    postgres=# \du;
    ```
