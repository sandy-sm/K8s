#### Theory

Docker security

* When you run a container in docker. it by default runs as root user
* A root user is having lot many super privileges which could be dangerous
* Docker provides a way to specify USER 1001 in Dockerfile to run the container with that user. 1001 is the user id
* In linux, the capability of the user is defined in "/usr/include/linux/capability.sh"
* docker run --cap-add MAC_ADMIN ubuntu


Security context

* Similarly in k8s we specify the capabilities in pod definitions as below


to check user

> k exec ubuntu-sleeper -- whoami


> k replace --force -f /tmp/pod.yaml



