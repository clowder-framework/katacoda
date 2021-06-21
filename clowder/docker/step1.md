# The docker-compose File(s)

We will use docker-compose to run Clowder. In this scenario we have provided you with the files that are needed to start clowder using docker-compose. 

The first file, docker-compose.yml, is the default that is distributed on [GitHub](https://github.com/clowder-framework/clowder/blob/develop/docker-compose.yml). This has all the required componnets of Clowder as well as some optional ones:

- Clowder
- MongoDB
- ElastSearch
- RabbitMQ

Check out the second file, docker-compose.override.yml, This will override the default fil and open a port for RabbitMQ as well as add the image preview extractor.

```
cat docker-compose.override.yml
```{{execute}}

This file also add overrides for the folders, so they are saved outside of docker.