### Requirements

Install Docker

Docker Engine with Swarm mode activated (by either init/join Swarm)

### Prerequisite

You need to create overlay network called `classvar-traefik-lb` externally and explicitly.

run the command:
```bash
$ docker network create -d overlay classvar-traefik-lb
```

### Deploy, Update Swarm

Docker Swarm provides simple commands for deployment

run the command:

```bash
$ DOMAIN=localhost ADMIN_USER=classvar HASHED_PASSWORD=$(openssl passwd -apr1 classvar) docker stack deploy -c docker-compose.yaml classvar
```

### Remove Swarm

```bash
$ docker stack rm classvar
```