
#### Rollback to previous Revision
```sh
kubectl rollout undo deployment/gta-deployment --to-revision=1

kubectl get rs

kubectl describe deployment gta-deployment

kubectl rollout history deployment/gta-deployment
```