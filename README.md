# Calibre - E-book management

## Deploy

```shell
docker-compose up -d
```

## Deploy with nginx

deploy

```shell
docker-compose up -d
```

and set the following location block in nginx:

```
location /calibre-web {
    proxy_pass              http://<your-ip>:8083;
    proxy_set_header        Host            $http_host;
    proxy_set_header        X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header        X-Scheme        $scheme;
    proxy_set_header        X-Script-Name   /calibre-web;
}
```

