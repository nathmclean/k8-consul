# k8-consul

Kubernetes deployment descriptors to deploy a consul cluster (of three) servers.

Tested on [Minikube](https://github.com/kubernetes/minikube) v0.10.0, on MacOS 10.12, kubectl 1.3.

## How to Use

```shell
kubectl create -f volumes.yaml
```

loging to the virtual box instance running minikube and open the file permissions on /data (I used 777, but less open permissions should work...)

```shell
kubectl create -f services/
kubectl create -f deployments/
```

## View whats been created

```shell
eval $(minikube docker-env) #This will set your docker env so that you can interact with containers running in minikube
docker ps # see Whats running
```

Open the kubernetes dashboard in a browser.
```shell
minikube dashboard
```
