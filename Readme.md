# Install grafana on kubernetes
It is recommended to create a new namespace in Kubernetes to better manage, organize, allocate, and manage cluster resources. For more information about Namespaces, refer to the official Kubernetes documentation.
## To create a namespace, run the following command:
```
kubectl create namespace my-grafana
```
In this example, the namespace is my-grafana
## To verify and view the newly created namespace, run the following command:
```
kubectl get namespace my-grafana
```
The output of the command provides more information about the newly created namespace.
## Create PV for storing data
```
kubectl apply -f pv.yaml
```
## run the following command for deploying grafana
```
kubectl apply -f grafana.yaml -n my-grafana
```
## expose application using ingress
```
kubectl apply -f ingress.yaml
```
