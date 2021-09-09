### Deploy mysql using persistent volume
```console
  helm search hub mariadb
  helm repo add bitnami https://charts.bitnami.com/bitnami
  helm show values bitnami/mariadb > values.yml
  
  config on demand in values.yml
    config line 90 architecture: replication    
    config from line 95 auth:...
    config primary:...
      persistent.storageClass: "nfs-client"    
    config secondary similar primary ...
  helm install my-release bitnami/mariadb -f values.yaml
```
### Ref
- https://artifacthub.io/packages/helm/bitnami/mariadb
- https://engineering.bitnami.com/articles/deploy-a-production-ready-mariadb-cluster-on-kubernetes-with-bitnami-and-helm.html