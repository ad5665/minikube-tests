# Namespaces

## How to apply Namespace
```bash
kubectl create -f .\namespaces\namespace-dev.yaml
namespace/ns-dev created

kubectl create -f .\namespaces\namespace-prod.yaml
namespace/ns-prod created

kubectl get namespaces
NAME              STATUS   AGE
default           Active   47m
kube-node-lease   Active   47m
kube-public       Active   47m
kube-system       Active   47m
ns-dev            Active   20s
ns-prod           Active   15s

```