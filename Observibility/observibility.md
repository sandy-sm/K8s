### Pod lifecycle (STATUS)

* Pod can be in one of the below state: Pending, ContainerCreating, Running
* Pending - Pod is not yet placed on node by scheduler
* ContainerCreating - Pod is getting ready, downloading required images 
* Running - Pod is started and up and running

### Pod Conditions

* Conditions complements pod status and gives detailed information 
* PodScheduled, Initialized, ContainerReady, Ready
* PodScheduled - (true/false) - pod scheduled on a node
* Initialized - (true/false) - pod is initialized
* ContainerReady --   all containers are ready
* Ready -- pod is ready

