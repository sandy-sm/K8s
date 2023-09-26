
### Theory

* When you create deployment — it creates replicates as well.

Deployment capabilities
* rolling update of app versions
* Upgrading environment
* Scaling
* Pause and run


## Commands

Deployments: (same like replicates except kind: Deployment)

> k get deploy


Create deploy using file

> k create -f deployment-definition.yaml

Alternatively,

> k create deploy https-frontend —image=httpd:2.14-alpine —replicas=3


