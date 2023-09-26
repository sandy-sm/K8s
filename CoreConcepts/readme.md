
#### Components of Kubernetes

* **API Server**: Frontend of the k8s. Exposes endpoints and API to CLI
* **Scheduler**: Schedules /assigns new pods on nodes
* **Controller**: Brain behind the k8s who decides the new master node in case of failure and other pod failures as well, it brings up pods on failure
* **Container** Runtime: Docker, other like rocket or trio
* **Kubelet**: agent client command which talks to API server
* **etcd** : distributed key-value store which store information about node metadata.


#### Master vs worker node:

Worker node:  container runtime such as Docker,
		contains kubelet agent which responds to kibe-api server
		etcd
		controller
		scheduler

Master node: contains kube-api server

Kubectl: kube control or kube command line tool, anything and everything to talk to k8s server

Container runtime interface: provided by k8s to let container runtime vendors work with k8s

Docker runtime was being worked with dockershim - hacky way to support docker

Containerd - was another runtime that supports CRI

K8s was made to orchestrate docker.
K8s grew in popularity. The other vendors want to come in

Open container initiative - imagespec (how image is build) and runtimespec (how runtime container must be developed)

Rkt and crio supports k8s via CRI


Containerd is a separate runtime.

K8s v1.24+ remove dockershim

— ctr comes with containerd not very user friendly though


#### Nerdctl
* nerdctl provides docker like cli for containerd
* Nerdctl supports docker compose

#### Crictl
* crictl provides cli for CRI compatible runtimes
* Installed separately 


When you create deployment — it creates replicas as well.

#### Deployment capabilities

* rolling update of app versions
* Upgrading environment
* Scaling
* Pause and run

