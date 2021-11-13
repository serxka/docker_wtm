# docker_wtm
If you want to host elsewhere, modify relevant domain and settings in the `/conf` folder.

To create the certificates:
```
docker-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ -d moth.knao.net
```
In order to renew certificates:
```
docker-compose run --rm certbot renew
```

To start and run it: `docker-compose up --build -d`
