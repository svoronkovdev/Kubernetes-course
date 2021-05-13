# Kubernetes-course

## Minicube

`minicube version`   -show version of minicube

`minicube start`     -create and run k8s with default parameters

`minicube stop`      -stop minicube

`minicube delete`    -delete minicube with cluster

`minicube ssh`      -create login with our cluster


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

`kubectl port-forward hello 7777:80` - Our port 7777 now is port 80 our pod

`kubectl describe pods hello` -show all inf about pod hello

`kubectl delete pods hello`  -delete pod hello

`kubectl logs hello` -show log from pod hello

`kubectl exec my-web date` -run command date on pod my-web

`kubectl exec -it my-web bash` -run command bash interactively on pod my web

`kubectl apply -f myfile.yaml` -create objects in k8s from file myfile.yaml

`kubectl delete -f myfile.yaml` -delete objects from k8s from file myfile.yaml
