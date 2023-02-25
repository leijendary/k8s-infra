# Kubernetes Development Environment

1. Create volume directories:

```
sudo mkdir -p /Volumes/Kubernetes
sudo mkdir /Volumes/Kubernetes/redis
sudo mkdir /Volumes/Kubernetes/postgres
sudo mkdir /Volumes/Kubernetes/elasticsearch
sudo mkdir /Volumes/Kubernetes/kafka

sudo chmod 777 /Volumes/Kubernetes/*
```

2. Apply all services:

```
kubectl apply -f cache
kubectl apply -f database
kubectl apply -f elasticstack
kubectl apply -f kafka
kubectl apply -f metrics-server
kubectl apply -f monitoring
```

## Commands

Most used commands for checking the services

1. Check the status of the pods in a given namespace:

   `kubectl get pods -n <namespace>`

2. Get all details of a pod:

   `kubectl describe pods <service> -n <namespace>`

3. Get logs of a pod:

   `kubectl logs -f <pod name> -n <namespace>`
