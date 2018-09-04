# PostgreSQL

## Docker usage

### Take a dump from a running postgres container

```bash
# Backup entire database
docker exec -t <container> pg_dumpall -c -U postgres | gzip > dump.sql

# Restore backup
cat dump.sql | docker exec -i <container> psql -U postgres
```

