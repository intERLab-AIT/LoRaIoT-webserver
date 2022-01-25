# LoRaIoT Webserver

Nginx server with cryptbot.  Reverse proxying ttn3 stack and lorarelay.

To start server.
```
docker-compose up -d loraiot-webserver
```

To generate Cert.

```
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/  -d ttn.hazemon.in.th
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/  -d lora.hazemon.in.th
```


To renew certs (every 3 months)
```
docker-compose run --rm certbot renew
```
