# 💼 suitcase

Launch all my services with Docker

* [Plex Server](https://www.plex.tv/)
* [Iron-Cake](https://github.com/JoseFilipeFerreira/iron-cake): Simple Webserver
* [JBB.py](https://github.com/josefilipeferreira/JBB.py): Discord bot
* [Radicale](https://radicale.org/v3.html): CalDav and CardDav Server
* [Merossd](https://github.com/josefilipeferreira/merossd): Control meross lights
* [rss-bridge](https://github.com/RSS-Bridge/rss-bridge): RSS feed generator for websites


## Nginx configuration

```
server {
        server_name jff.sh;

        listen 80;

        location / {
                proxy_pass http://127.0.0.1:8000/;
        }

        location /radicale/ {
                proxy_pass        http://localhost:5232/;
                proxy_set_header  X-Script-Name /radicale;
                proxy_set_header  X-Forwarded-For $proxy_add_x_forwarded_for;
                proxy_set_header  Host $http_host;
                proxy_pass_header Authorization;
        }

        location /rss-bridge/ {
                proxy_pass        http://localhost:3000/;
        }


}
```
