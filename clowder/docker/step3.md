# Starting Clowder

We are now ready to start clowder. All the containers can be started using the docker-compose command. If no file argument is given, it will use the `docker-compose.yml` file, as well if it exists, the `docker-compose.override.yml` file.

```
docker-compose up -d
```{{execute}}

The RabbitMQ and MongoDB containers will take some time to start, during this time it is normal for the extractors and clowder to crash. Once these containers have started, clowder and all containers should start correctly as well.

Lets check on the containers:

```
docker-compose ps
```{{execute}}


Once the clowder container shows `healthy` and all other containers are up, we are ready to continue. You can see the clowder user iterface at Render port 9000: https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com/. However at this point there are no users and we can't login.
