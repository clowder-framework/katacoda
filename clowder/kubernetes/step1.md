First we need to make sure all the pre-requisites are met to run clowder in kubernetes using HELM.

The helm chart assumes version 3 of helm. Lets make sure we have the right version:
`helm version`{{execute}}

Next we want to make sure kubernetes is ready and at least version 1.14
`kubectl get nodes`{{execute}}

Finally, we want to make sure a storageclass is defined
`kubectl get storageclass`{{execute}}


Next we will install the repository where clowder can be found
