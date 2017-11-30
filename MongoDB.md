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
