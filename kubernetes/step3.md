Clowder has many options that can be set. The helm chart will have many default values. We will set a few common values:
- set the admin key
- add the first user
- set storageClass (since there is no default)

```
cat << EOF > katacoda.yaml
storage: &storage local-storage

commKey: katacoda

initialAdmins:
  - admin@example.com

users:
  - email: admin@example.com
    firstname: Admin
    lastname: User
    admin: true
    password: katacoda

persistence:
  storageClass: *storage

elasticsearch:
  persistence:
    storageClass: *storage

rabbitmq:
  persistence:
    storageClass: *storage

mongodb:
  persistence:
    storageClass: *storage
EOF
```{{execute}}

