#### Documentation Reference:

https://github.com/kubernetes-sigs/metrics-server

#### Install Metric Server
```sh
kubectl apply -f metric-server.yaml
```
#### Verify 
```sh
kubectl top pods
kubectl top nodes
```
