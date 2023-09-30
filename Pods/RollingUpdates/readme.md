Rollouts and versioning

* when you create new deployment, it creates revision rollout with new version 
* rollout command
> k rollout status deployment/my-deployment

* Deployment strategy
   * Recreate
     * Bring older version down
     * Start new version.
     * there could be downtime 
   * Rolling
     * one version down, one version up
     * default strategy

* Updating image
  * modify deploy-config.yaml
  * OR
  * k set image deployment/mydeployment nginx-container=nginx:latest
  * k set image <<deployment-name>> <<container-name>>=<<image-name>>:<<version>>
    * update deployment-definition.yaml

* k describe deployment my-deployment (check events)

* ReplicaSets is created under the hood
* 1 old replicasets, 1 new replicasets
* > k get replicasets
  

* if you like to rollback to previous version
  * > k rollout undo deployment/my-deployment
    
Summarize commands:

1) Create a deployment

> k create -f deployment-config.yaml

2) Get Deployment

> k get deployments


3) Update
> k apply -f deployment-definition.yaml
> k set image deployment/my-deployment nginx-container=nginx:latest

4) Rollout status

> k rollout status deployment/myapp-deployment


5) See history

> k rollout history deployment/myapp-deployment


6) Rollback

> k rollout undo deployment/myapp-deployment


7) Rollback to specific version

> k rollout undo deployment/myapp-deployment --to-revision=2