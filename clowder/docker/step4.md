At this point we have clowder up and running. Before we can login, we need to add the first user to the system. Additional users can be done using the signup, however the first user needs to be done manually since there are no adiministrators at this point to approve the user.

```
docker run --rm -ti --network root_clowder \
	-e FIRST_NAME=Admin \
	-e LAST_NAME=User \
    -e EMAIL_ADDRESS=admin@example.com \
    -e PASSWORD=catsarecute \
    -e ADMIN=true \
	clowder/mongo-init
```{{execute}}

At this point we can login into clowder https://[[HOST_SUBDOMAIN]]-9000-[[KATACODA_HOST]].environments.katacoda.com/

- username `admin@example.com`{{copy}}
- password `catsarecute`{{copy}}
