Clowder has many options that can be set. The helm chart will have many default values. We will set a few common values:
- set the admin key
- add the first user
- set storageClass [1]

Check out the settings.

```
cat katacoda.yml
```{{execute}}

MongoDB and ElasticSearch, as all other databases, require a storage with fast IOPS, in general it is not recommended to use NFS for database storage.

[1] Most kubernetes clusters will have a default storage class which will be used. In this case there is none, and we specify explicitly what storage class to use.
