```shell
docker node update --label-add laravel.webserver-data=true $NODE_ID
```

```shell
docker node update --label-add laravel.app-data=true $NODE_ID
```

```shell
docker node update --label-add laravel.queue-worker-data=true $NODE_ID
```

```shell
docker node update --label-add laravel.schedule-runner-data=true $NODE_ID
```

```shell
cp example.env .env
```

```shell
vim .env
```

```shell
cp app/example-php.ini app/php.ini
```

```shell
cp webserver/conf.d/example.conf webserver/conf.d/default.conf
```

```shell
eval $(egrep "^[^#;]" .env | xargs -d'\n' -n1 | sed 's/^/export /') && \
docker stack deploy -c laravel.yml laravel
```
