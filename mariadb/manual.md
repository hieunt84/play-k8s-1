### Deploy mysql using persistent volume
```console
  helm search hub mariadb
  helm repo add bitnami https://charts.bitnami.com/bitnami
  helm show values bitnami/mariadb > values.yml
  config on demand in values.yml
    config line 90 architecture: replication
    config line 280 primary.resources.limit
    config line 285 primary.resources.requests
    config line 378 primary.persistent.storageClass: "nfs-client"
    config secondary similar primary

  helm install hit-mariadb bitnami/mariadb -f values
```
### Ref
- https://artifacthub.io/packages/helm/bitnami/mariadb