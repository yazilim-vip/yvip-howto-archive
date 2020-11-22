
## Backup & Restore Operasyonları

### Backup
**Postgresql Custom Dump Formatında backup:** \
`pg_dump -h HOST -p PORT -U PG_USER -W -Fc DB > BACKUP_FILE_PATH`

**SQL Formatında Backup Almak** \
`pg_dump -h HOST -p PORT -U USER -W --data-only --column-inserts  DATABASE_NAME > BACKUP_FILE_PATH`

**Text Tabanlı Backup:** \
`pg_dump -h HOST -p PORT -U USER -W  DB_NAME > dump-file-path`

|Parametreler| Açıklamaları |
|-|-------|
| -W | komut çalıştırılırken -U ile verilen kullanıcının şifresi girmesini beklenir. |
| -a, --data-only | Dump only the data, not the schema (data definitions). Table data, large objects, and sequence values are dumped. |
| -s, --schema-only |    Dump only the object definitions (schema), not data. |
| --column-inserts |  Dump data as INSERT commands with explicit column names (INSERT INTO table (column, ...) VALUES ...). |


### Restore
**Postgresql Custom Dump Formatında restore**: \
`pg_restore -h HOST -p PORT -U PG_USER -W -d  BACKUP_FILE_`

**Postgresql Custom Dump Formatında restore:** \
`psql -h HOST -p POSRT -U PG_USER -W -d DB_NAME -f BACKUP_FILE_`

### NOT
|||
|:-:|-------|
| HOST | postgresql server'ın kurulu olduğu makineye erişim için kullanılan adres |
| PORT | postgresql server'ın kurulu olduğu makineye erişim için kullanılan port |
| USER | postgresql server'da dump edilecek olan veritabanı üzerinde gerekli yetkileri olan kullanıcı adı |
| DB_NAME | backup/restore yapılacak veritabanının adı |
