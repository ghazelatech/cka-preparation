#### Documentation Reference:

https://kubernetes.io/docs/concepts/workloads/controllers/deployment/

#### Create a new Deployment 
```sh
kubectl create deployment gta-deployment --image=nginx
```
```sh
kubectl get pods
```
#### Set a New Image to Existing Deployment
```sh
kubectl set image deployment/gta-deployment nginx=apache
```
```sh
kubectl get pods
```
#### Rolling Back changes
```sh
kubectl rollout history deployment gta-deployment
```
```sh
kubectl rollout undo deployment/gta-deployment
```
#### Adding a Record Instruction
```sh
kubectl set image deployment/gta-deployment nginx=httpd
```
```sh
kubectl rollout history deployment gta-deployment
```
#### Scaling Deployment

```sh
kubectl scale deployment/gta-deployment --replicas=10
```
```sh
kubectl get deployments
kubectl get pods
```

#### Delete the resources created in this lecture
```sh
kubectl delete deployment gta-deployment
```