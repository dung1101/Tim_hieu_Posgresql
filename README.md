# Tim_hieu_Posgresql
```
PGPASSWORD="super_hard_to_guess" pg_dump --no-owner -h 127.0.0.1 -p 5432 -Z0 -Fc -U super_user xanderp > export.psql
PGPASSWORD="super_hard_to_guess" psql -h 127.0.0.1 -p 5432 -U super_user xanderp < export.psql
```
[Tutorial](http://webfaver.com/database/huong-dan-backup-va-restore-postgres-database.html)
