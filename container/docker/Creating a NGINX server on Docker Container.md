Creating a NGINX server on Docker Container

Parametrelerin Açıklamaları:
*  `--name`: Oluşturulacak olan Docker Container'ın
*  `--v`: Container içerisinideki bir dizini HOST üzerindeki bir dizine mount etmek için kullanılır. kullanılma amacı, nginx docker container içerisindeki nginx ile ilgili ayarları bağlamak için kullanılmıştır.
*  `-d`: container'ın arka planda çalışmasını sağlar

Command : \
`docker run --name yvip-nginx -v /home/yazilimvip/nginx:/etc/nginx/conf.d:z -d nginx `