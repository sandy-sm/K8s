* K8s does not provide inbuilt monitoring 
* Monitoring kubectl nodes, pods and the resource (cpu/mem) consumption can be done in below ways
* Metrics Server (open source)
* Prometheus (paid)
* ElasticStack
* DataDog
* dynatrace
* 1 metrics server per cluster
* in -memory monitoring solution
* An agent kubelet (cAdvisor) retrieve metrics data
  * minikube addons enable metrics-server
  * OR
  * git clone https://github.com/kubernetes-incubator/metrics-server.git
  * cd metrics-server
  * > k create -f .
* k top node
* k top pods