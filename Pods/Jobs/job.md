Jobs

* batch processing /analytics and reporting tasks just start and stop
* For such applications, kubernetes supports the kind: Job
* Just like replica-sets, Job is used to manage short-lived application jobs
* deleting job also deletes the pods
* persistentVolume is typically used to generate and/or preserve the output from pod
* To run multiple instance of job we specify
    > completions: 3
* desired count:3
* by default : pod is created one after another
* if pod fails, it creates again until all completions 
* to parallely run
  > parallelism: 3
  > completions: 3
* 3 pods created at once, if 1 fails it re-creates