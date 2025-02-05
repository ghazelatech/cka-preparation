### nodeAffinity-required.yaml
```sh
apiVersion: v1
kind: Pod
metadata:
  name: gta-node-affinity
spec:
  affinity:
    nodeAffinity:
      requiredDuringSchedulingIgnoredDuringExecution:
        nodeSelectorTerms:
        - matchExpressions:
          - key: disk
            operator: In
            values:
            - ssd2
  containers:
  - name: with-node-affinity
    image: nginx
```

### nodeAffinity-preferred.yaml
```sh
apiVersion: v1
kind: Pod
metadata:
  name: gta-node-affinity-preferred
spec:
  affinity:
    nodeAffinity:
      preferredDuringSchedulingIgnoredDuringExecution:
      - weight: 1
        preference:
          matchExpressions:
          - key: memory
            operator: In
            values:
            - high
            - medium
  containers:
  - name: gta-affinity-prefferd
    image: nginx
```
