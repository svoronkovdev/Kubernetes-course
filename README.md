# Kubernetes-course

## Minicube

minicube version   -show version of minicube

minicube start     -create and run k8s with default parameters

minicube stop      -stop minicube

minicube delete    -delete minicube with cluster

minicube ssh       -create login with our cluster


minicube start --cpus=4 --memory=8gb --disk-size=5gb       -start with defined parameters

minicube start --cpus=2 --memory=6000mb --disk-size=4000mb -start with defined parameters

## Kubectl

kubectl version              -show version of kubectl client and server

kubectl version --client     -show version of kubectl client

kubectl get componentstatuses -show state of cluster

kubectl cluster-info          -show info about k8s cluster

kubectl get nodes             -show  all servers k8s cluster
