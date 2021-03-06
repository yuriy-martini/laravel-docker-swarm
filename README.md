```shell
git clone https://github.com/yuriy-martini/laravel-docker-swarm
```

```shell
docker swarm init
```

```shell
docker swarm init --advertise-addr x.x.x.x
```

```shell
export NODE_ID=$(docker info -f '{{.Swarm.NodeID}}')
```

```shell
docker network create --driver=overlay traefik-public
```

```shell
docker network create --driver=overlay db-public
```

## Stacks

1. [traefik](traefik/README.md)
1. [db](db/README.md) (optional)
1. [laravel](laravel/README.md)
