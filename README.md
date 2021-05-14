# Kubernetes-course

## Minicube

`minicube version`   -show version of minicube

`minicube start`     -create and run k8s with default parameters

`minicube stop`      -stop minicube

`minicube delete`    -delete minicube with cluster

`minicube ssh`      -create login with our cluster

`minikube start --nodes 2 -p multinode-demo`  - 2 nodes

`minicube start --cpus=4 --memory=8gb --disk-size=5gb`       -start with defined parameters

`minicube start --cpus=2 --memory=6000mb --disk-size=4000mb` -start with defined parameters

## Kubectl

`kubectl version`              -show version of kubectl client and server

`kubectl version --client`     -show version of kubectl client

`kubectl get componentstatuses` -show state of cluster

`kubectl cluster-info`          -show info about k8s cluster

`kubectl get nodes`             -show  all servers k8s cluster

## AWS

Install awscli, kubectl, eksctl

Kubernetes - eksctl configuration(https://eksctl.io) Place config(~/.kube/config)

`eksctl create cluster -f mycluster.yaml`    -create and run k8s cluster with file parameters

`eksctl delete cluster -f mycluster.yaml`    -delete our k8s cluster

`eksctl version`                             -show eksctl version

`eksctl create cluster`                      -create default cluster

`eksctl delete cluster`                      -delete cluster

## GCP(Google cloud)

Need to install google cloud sdk

`gcloud version`                                   -show version of gcloud

`gcloud init`                                      -setting gcloud with your Cloud

`gcloud services enable container.googleapis.com`  -turn on creating k8s in your google cloud project

`gcloud container clusters create name`            -create and run k8s cluster with default parameters

`gcloud container clusters create name --num-nodes=4` -create and run cluster with our parameters

`gcloud container clusters get-credentials name`     -setting up kubectl for work with our cluster

`gcloud container clusters delete name`              -delete our cluster

## Pods

`kubectl get pods`    -show all pods

`kubectl run hello --generator=run-pod/v1 --image=nginx:latest --port=80` -create pod from dockerImage nginx and open port 80

` --generator=run-pod/v1 ` -for google in minicube not needed

`kubectl port-forward hello 7777:80` - Our port 7777 now is port 80 our pod

`kubectl describe pods hello` -show all inf about pod hello

`kubectl delete pods hello`  -delete pod hello

`kubectl logs hello` -show log from pod hello

`kubectl exec my-web date` -run command date on pod my-web

`kubectl exec -it my-web bash` -run command bash interactively on pod my web

`kubectl apply -f myfile.yaml` -create objects in k8s from file myfile.yaml

`kubectl delete -f myfile.yaml` -delete objects from k8s from file myfile.yaml


## Deployments

`kubectl get deployments`    -show all deployments

`kubectl get rs`    -show all replicaSets

`kubectl create deployment name-deployment --image httpd:latest`    -create deployment from dockerImage httpd:latest

`kubectl describe deployments name-deployment`    -show all info about deployment name-deployment

`kubectl scale deployment name-deployment --replicas 4`    -create replicaSets

`kubectl autoscale deployment name --min=10 --max=15 --cpu-percent=80`    -create autoScaling for deployment name

`kubectl get hpa`    -show all HPA- Horizontal Auto Scallers

`kubectl set image deployment/name-deployment k8sphp=adv4000/k8sphp:version2 --record`    -set deployment name Image to new

`kubectl rollout status deployment/name-deployment`    -show status updating

`kubectl rollout history deployment/name-deployment`    -show history updating

`kubectl rollout undo deployment/name-deployment`    -rollback to previous version

`kubectl rollout undo deployment/name-deployment --to-revision=2`    -rollback to version 2

`kubectl rollout restart deployment/name-deployment`    -redeploy current version

`kubectl delete deployments name-deployment`    -delete deployment name-deployment
