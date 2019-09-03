# kubernetes-playground

# To run the guestbook with replication controller
Working multi-tier application deployed on Kubernetes and Docker. In this scenario we introduced the core concepts of Kubernetes. We explained how Replication Controllers define how a container should be run. The service is used to determine how to proxy traffic to the container. Finally, everything is run as Pods. Once running the service can be accessed via the defined NodePort.

- kubectl create -f redis-master-controller.yaml
- kubectl create -f redis-master-service.yaml

- kubectl create -f redis-slave-controller.yaml
- kubectl create -f redis-slave-service.yaml

- kubectl create -f frontend-controller.yaml
- kubectl create -f frontend-service.yaml

- kubectl describe service frontend | grep NodePort

