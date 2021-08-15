docker network create -d overlay traefik-public

DOMAIN=localhost ADMIN_USER=classvar HASHED_PASSWORD=$(openssl passwd -apr1 classvar) docker stack deploy -c docker-compose.traefik.yml swarmprom