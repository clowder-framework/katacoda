We will use docker-compose to run Clowder. In this scenario we have provided you with the files that are needed to start clowder using docker-compose. 

If you look a the `docker-compose.yml` file you will see it is a slightmly modified version of the default that is distributed on [GitHub](https://github.com/clowder-framework/clowder/blob/develop/docker-compose.yml). 

```
cat docker-compose.yml
```{{execute}}

This has all the required componets of Clowder, but has all configuration variables removed, and the version of clowder is pinned to 1.17. The file will start the following containers:

- Clowder
- MongoDB
- ElastSearch
- RabbitMQ


Check out the second file, docker-compose.override.yml, This will override the default file and open a port for RabbitMQ as well as add the image preview extractor. This file also add overrides for the folders, so they are saved outside of docker.

```
cat docker-compose.override.yml
```{{execute}}
