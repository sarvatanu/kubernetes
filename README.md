# kubernetes

Kubernetes is a open sourced framework for automatic deployment, scaling and managing the container based application.

# Minikube
 Install Minikube, virtualbox and kubectl for local kubernetes deployment. Refer online for OS specicifc commands or
 
 1. brew cask install minikube
 2. brew install kubectl
 
Note : virtual box should be installed

* Current context : 
 kubectl config current-context which will display minikube
 
# Master Node

   * Kube API Server
     * Scheduler for scheduling the contaier,
     * cluster store etcd : 
     * API Controller (watcher) for managing the endpoints like namespace endpoints, node endpoints etc
   * Nodes
     * Kubelet agent : reposible for reporting to master
     * kube proxy : load balancer
     * container  runtime: like rocket(rkt) or docker
# Pods
# Services
# Replica set
# Deployments
