# Consul

```bash
helm repo add hashicorp https://helm.releases.hashicorp.com
"hashicorp" has been added to your repositories

helm repo update
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "hashicorp" chart repository
Update Complete. ⎈Happy Helming!⎈

helm search repo hashicorp/consul
NAME                    CHART VERSION   APP VERSION     DESCRIPTION
hashicorp/consul        1.0.2           1.14.2          Official HashiCorp Consul Chart

##
#helm install --values .\consul\consul-vaules.yaml consul hashicorp/consul --create-namespace --namespace consul --version "1.0.2"
#helm install consul hashicorp/consul --set global.name=consul --create-namespace -n consul
## Failed to start consul-server

kubectl apply -f .\consul.yaml

❯ kubectl api-resources | grep deployment
deployments                       deploy                apps/v1                                true         Deployment
❯ kubectl api-resources | grep deploymentkubectl get statefulset | grep consul
❯ kubectl get statefulset | grep consul
consul   0/5     4m52s

## failing on multi node minikube - https://github.com/kubernetes/minikube/pull/15062
## works on single node cluster
helm install consul hashicorp/consul --set global.name=consul --create-namespace -n consul

```