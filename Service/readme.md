
### Theory



### Imperative commands

Create a service named redis-service to expose redis app on port 6379


> k expose po redis --port 6379 --name redis-service 


Create a new pod httpd using image httpd-alpine in default namespace,
next create a service of type clusterip by same name httpd

> k run po httpd --image=httpd:alpine --port=80 --expose=true

service/httpd created
pod/httpd created



