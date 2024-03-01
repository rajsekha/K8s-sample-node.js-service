# K8s-sample-node.js-service
This project is created using avaliable sample Hello-world node.js service image from internet for deployment of kubernetes applications.
This service expose 3 apis:

/ping
/current-date
/fibo/:n

Deploying in the Kubernetes cluster:

First create the Pod using deployment.yaml file

kubectl apply -f kubernetes/deployment.yml

check the pod status

kubectl get pod

Exposing the Api to the World: 
Deploy service.yaml file in Kubernetes cluster

kubectl apply -f kubernetes/service-external.yml

Checking:

kubectl get service

service scalable by increasing the replica set

kubectl scale deployment hello-world-node --replicas=3



