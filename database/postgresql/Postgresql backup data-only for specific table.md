Postgresql backup data-only for specific table

```sql
pg_dump \
  -h 192.168.1.249 \
  -p 5432 \
  -U postgres -W \
  --table="public.splitlib" \
  --data-only \
  --column-inserts \
  DATABASE_NAME > FILE_NAME.sql
```