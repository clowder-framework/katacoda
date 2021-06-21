As you could see before we added overrides to the docker-compose to make sure the data for clowder is saved on the local file system, and not in the docker container.

```
volumes:
  clowder-data:
    driver_opts:
      type: none
      device: '${PWD}/volumes/clowder-data'
      o: bind
```

For docker to be able to write to this folder we need to make sure it exists, and the permissions are correct.

```
mkdir -p ${PWD}/volumes/{clowder-data,clowder-custom,mongo}
chmod 777 ${PWD}/volumes/*
```{{execute}}

At this point we are ready to start clowder.
