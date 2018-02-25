# kubernetes  sample Edit

Kubernetes is a open sourced framework for automatic deployment, scaling and managing the container based application.

# Minikube
 Install Minikube, virtualbox and kubectl for local kubernetes deployment. Refer online for OS specicifc commands or
 
 1. brew cask install minikube
 2. brew install kubectl
 
Note : virtual box should be installed

* Current context : 
 kubectl config current-context which will display minikube
 
# Master Node

   * Kube API Server : Main gateway in Kubernetes
     * Scheduler for scheduling the contaier,
     * cluster store etcd : 
     * API Controller (watcher) for managing the endpoints like namespace endpoints, node endpoints etc
   * Nodes
     * Kubelet agent : responsible for reporting to master
     * kube proxy : load balancer
     * container  runtime: like rocket(rkt) or docker
# Pods
 contains group of corelated contains. To create pods



 
 * minikube start
 * kubectl get pods --> to check current pods
 * kubectl create -f filepath 
   * File path ex: /Users/saravanan/personal/projects/kubernetes
 * kubectl describe pods --> to check the activities
 * kubectl get pods --show-labels --> to show labels
 * kubectl logs name --> pass name of the pod to get the logs
* Display dashboard using 'minikube dashboard'
# Services
 With mortal nature of the pods(can come up and go down any time), serviecs will be best option for service discover to connect to available pods
 
 Services can have static IP, DNS, Port 
 
 From Client --> Service --> Pods
 
 * kubectl create -f service.yml
 * kubectl describe svc
 * kubectl get service (svc or service keyword)
 
 * kubectl create -f replicaController.yml --> rc getting phasedout in favour replication set.
 * kubeclt describe rc
 
 Note: label on pods should match selector label on service.yml
 
to launch the service : 

* minikube service house-api-svc-v1

on the launched URL use /api/house
# Replica set
# Deployments
 Is a new thing in Kubernetes
