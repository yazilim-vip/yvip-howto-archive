
Docker üzreinde kurulmuş olan PostgreSQL veritabanında sadece `postgres` kullanıcısının superuser olarak tanım olduğunu varsayalım. Eğer `postgres` kullanıcısının login yetkisi silinir ise sisteme PostgreSQL veritabanına hiç bir şekilde giriş yapılamamaktadır. Giriş yapılması denendiğinde ise aşağıdaki gibi bir hata alınacaktır: \

```role "xyz" is not permitted to log in```

Sorunun çözümü içn uygulanması gereken adımlar:

1. Yeni bir PostgreSQL veritabanı kurulur (Docker dışında, VM olabilir)
2. Ardından, Docker içerisinde yer alan PostgreSQL sunusunun, data klasörü, lokale taşınır.
3. Yeni kurulan PostgreSQL veritabanının data klasörü eski PostgreSQL veritabanının data'sı olarak ayarlanır
	- Link: https://www.digitalocean.com/community/tutorials/how-to-move-a-postgresql-data-directory-to-a-new-location-on-ubuntu-16-04
4. Yeni kurulan PostgreSQL veritabanı single user mod ile çalıştırılır.
    - ```bash postgres --single -D /path/to/pgdata ```
	- Link: https://www.postgresql.org/message-id/2c72583f-6458-a334-496b-3f3ec368f8d5%40dalibo.com