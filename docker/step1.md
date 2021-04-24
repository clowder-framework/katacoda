# Starting Clowder using Docker

Create the folders:

Before we start clowder, we need to make sure the folders are created for clowder and mongo, and have the right permissions:

```
mkdir -p ${PWD}/volumes/{clowder-data,clowder-custom,mongo}
chmod 777 ${PWD}/volumes/*
```{{execute}}

Next we can start the clowder stack:
```
docker-compose up -d
```{{execute}}

And we can see clowder up and running.

Render port 9000: https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com/
