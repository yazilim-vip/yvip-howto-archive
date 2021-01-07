# Creating a NGINX on Docker Container

Parametrelerin Açıklamaları:
*  `--name`: Oluşturulacak olan Docker Container'ın
*  `--v`: Container içerisinideki bir dizini HOST üzerindeki bir dizine mount etmek için kullanılır. kullanılma amacı, nginx docker container içerisindeki nginx ile ilgili ayarları bağlamak için kullanılmıştır.
*  `-d`: container'ın arka planda çalışmasını sağlar

Command : \
`docker run --name yvip-nginx -v /home/yazilimvip/nginx:/etc/nginx/conf.d:z -d nginx `

Status check and reload of a running NGINX server on Docker Container

* Check Nginx configuration for correct syntax: \
    ` docker container exec <container> nginx -t`
* Reload Nginx inside Docker container: \
    `docker container exec <container> nginx -s reload`

**[Resource](https://www.shellhacks.com/docker-reload-nginx-inside-container/)**