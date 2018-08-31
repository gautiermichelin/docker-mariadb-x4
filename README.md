# Docker multiple DBs for mysql

Sometimes you need to isolate different dbs on the same server, to reduce or increase their used load.

This docker container project creates and runs 4 differents instances of MariaDB on port 3307, 3308, 3309 and 3310 on the same server. It was intended as a proof-of-concept for dividing mysql load, allowing to discrete resources such as a cpu limit of 0.25 for a particular server.

More informations on :

https://docs.docker.com/compose/compose-file/#resources