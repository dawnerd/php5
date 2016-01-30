php5
===

Optimized build of php for wordpress.

max_upload_size is set to 100M

Setup your `Dockerfile` like so:

```
FROM dawnerd/php5

ADD . /srv/www

EXPOSE 80

CMD service php5-fpm start && nginx
```

I've got production sites running this build with [nginx-proxy](https://github.com/jwilder/nginx-proxy) and [docker-letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion).
