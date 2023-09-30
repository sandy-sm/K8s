* labels and selectors are useful to group by pods based on functionality and/or other parameters.
* it allows you to view or use pods or resources effectively
* For e.g.
  * kubectl get pods --selector app=App1
* Replicaset and Deployment uses selectors to retrieve the pods
* Annotations: can be used for informative purpose. specifying buildVersion, author, phone-number etc.


```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
  labels:
    app: myapp
  annotations:
    buildVersion: 1.1
spec:
  containers:
    - name: nginx-container
      image: nginx
```

Cmd

Q) To print the count, instead of counting manually, useful when there are 100's of pods

> k get pods --selector env=dev --no-headers | wc -l

--no-headers -- does not print the header

Q) To search with multiple lables

> k get pods --selector env=dev,bu=finance,tier=frontend


