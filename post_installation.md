# Post Installation Configuration

## Environment Variables

```shell
$ vim ~/.profile
PATH=$PATH:/usr/lib/postgresql/9.5/bin
export PATH
$ . ~/.profile
```

### The Usable Binary Files

```shell
$ ls /usr/lib/postgresql/9.5/bin
clusterdb  createlang  dropdb    dropuser  oid2name           pg_basebackup   pg_ctl   pg_dumpall  pg_receivexlog  pg_resetxlog  pg_rewind   pg_test_fsync   pg_upgrade   pgbench   postmaster  reindexdb  vacuumlo createdb   createuser  droplang  initdb    pg_archivecleanup  pg_controldata  pg_dump  pg_isready  pg_recvlogical  pg_restore    pg_standby  pg_test_timing  pg_xlogdump  postgres  psql        vacuumdb
```

## Create a New Role

```shell
$ sudo -u postgres createuser --interactive
```

## Create a New Database

```shell
$ sudo -u postgres createdb database_name
```

## Add the Created Use

```shell
$ sudo adduser username
```

## Enable Remote Access

### Edit the Configuration File

```shell
$ vim /etc/postgresql/{version}/main/postgresql.conf
...
listen_address='*'
...
```

### Restart PostgreSQL for the Configuration File to Take Effect

```shell
$ invoke-rc.d postgresql restart
```
