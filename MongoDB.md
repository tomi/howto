# MongoDB

## Dump

Create a database dump

```bash
mongodump -d <database name> -o <target directory>
```

For example
```bash
DUMP_NAME=mongodump_`date "+%Y-%m-%d"`
mongodump -d <database name> -o $DUMP_NAME
tar -zcvf $DUMP_NAME.tar.gz $DUMP_NAME

```

Restore a database dump

```
mongorestore --db database_name path_to_directory
```

## Usage from docker

```bash
# Spin up a container
docker run -p 127.0.0.1:27017:27017 --mount type=bind,src=<abs_path_to_data_import>,dst=/datadump --name some-mongo -d mongo
# Restore data from dump
docker exec some-mongo mongorestore --db <dbname> /datadump
```
