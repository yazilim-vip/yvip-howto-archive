# Configure Postgresql Autobackup All DB

https://computingforgeeks.com/install-postgresql-12-on-ubuntu/

**CronJob:**
```
0 0 * * * /path/to/script 2>&1 | tee /path/to/logs
```