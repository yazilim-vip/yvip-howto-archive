# Index
* [howto-archive](/_user_manual_/howto_archive.md)
* [howto-react](/_user_manual_/howto_react.md)
* [howto-script](/_user_manual_/howto_script.md)
* **Docker**

# Docker
A RectJS web application that makes possible to browse your local HowTo Archive on browser.

If you wonder about what is HowTo Archive; You should check our HowTo Archive's structure: 
  * GitHub Repo: https://github.com/yazilim-vip/yvip-howto-archive
  * Showcase: https://howto.yazilim.vip

Other useful links:
* https://github.com/yazilim-vip/howto-script
* https://www.npmjs.com/package/@yazilim-vip/howto-script

# Usage

## Via docker-compose (recommended)
* Create a folder and create a file called `docker-compose.yml` under that folder
```yml
version: "3.4"
services:
  webapp:
    image: yazilimvip/howto-react:<version>
    ports:
      - "5100:80"
    environment:
      - "API_URL=http://localhost:5000"
    depends_on:
      - service
  service:
    image: yazilimvip/howto-script:0.10.2
    volumes:
      - /path/to/your/howto:/usr/src/app/howto
    ports:
      - "5000:5000"
```
* Run the following command to start containers
   ```bash
    docker-compose up -d
    ```

**IMPORTANT**
* In `docker-compose.yml` file do not forget to replace `/path/to/your/howto` with the path of your local HowTo Archive. 

## Without docker-compose
**IMPORTANT**
If you use HowTo React then first you should need a HowTo Service. To learn about starting  HowTo service you should check https://github.com/yazilim-vip/howto-script

If you had already have a running HowTo Service then start container with the following command
```bash
docker run \
  -e API_URL="<howto_service_base_url>" \
  -p <port>:80 \
  --name howto-webapp yazilimvip/howto-archive:<version>
```