https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/

#### Generic Commands:
```sh
systemctl status kubelet
cd /etc/systemd/system/kubelet.service.d
```

#### gta-pod.yaml
```sh
apiVersion: v1
kind: Pod
metadata:
  name: gta-pod
spec:
  containers:
  - name: gta-container
    image: nginx
```    
