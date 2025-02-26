# PHP docker images

## podman
```shell
podman build ./beanstalkd -t ghcr.io/vigicz/beanstalkd:0.1
podman build ./8.1-fpm -t ghcr.io/vigicz/php:8.1-fpm
podman build ./8.1-fpm-supervisord -t ghcr.io/vigicz/php:8.1-fpm-supervisor
```

## doc

```shell
docker build ./beanstalkd -t ghcr.io/vigicz/beanstalkd:0.1
docker build ./8.1-fpm -t ghcr.io/vigicz/php:8.1-fpm
docker build ./8.1-fpm-supervisord -t ghcr.io/vigicz/php:8.1-fpm-supervisor
```