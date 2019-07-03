# Docker multiple DBs for mysql

Sometimes you need to isolate different dbs on the same server, to reduce or increase their used load.

This docker container project creates and runs 4 differents instances of MariaDB on port 3307, 3308, 3309 and 3310 on the same server. It was intended as a proof-of-concept for dividing mysql load, allowing to discrete resources such as a cpu limit of 0.25 for a particular server.

More informations on :

https://docs.docker.com/compose/compose-file/#resources

## Prerequisites

### Install Docker

See https://docs.docker.com/install/linux/docker-ce/debian/

### Install Docker compose

See https://docs.docker.com/compose/install/

Summary for docker compose install
```
curl -L "https://github.com/docker/compose/releases/download/1.24.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

## Install

```
cd /var
git clone https://github.com/gautiermichelin/docker-mariadb-x4.git
cd docker-mariadb-x4
docker-compose create
docker-compose up 
```

Note : if you want to run docker-compose in the background

```
docker-composer up &
```

## Important informations

Datas are inside /var/docker-mariadb-x4/mariadb subfolders : db1 to db4.

## Error message about network ?
```
docker-compose up --force-recreate
```
