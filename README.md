# Useful PostgreSQL Queries

### Running queries

```sql
SELECT datid, datname, pid, usename, backend_start waiting, state, query 
FROM pg_stat_activity;
```

Alternatively, only active queries:

```sql
SELECT datid, datname, pid, usename, backend_start waiting, query 
FROM pg_stat_activity
WHERE state = 'active'
```
