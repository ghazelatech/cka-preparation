#### View previous rollout revisions
```sh
kubectl rollout history deployment/gta-deployment
```
#### Rolling Back to previous version of deployment
```sh
kubectl rollout undo deployment/gta-deployment --to-revision=1
```
