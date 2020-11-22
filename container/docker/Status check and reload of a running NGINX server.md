Status check and reload of a running NGINX server on Docker Container

Check Nginx configuration for correct syntax: \
` docker container exec <container> nginx -t`

Reload Nginx inside Docker container: \
`docker container exec <container> nginx -s reload`

**[Resource](https://www.shellhacks.com/docker-reload-nginx-inside-container/)**