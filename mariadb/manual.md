### Deploy mysql using persistent volume
```console
  helm search hub mariadb
  helm repo add bitnami https://charts.bitnami.com/bitnami
  helm show values bitnami/mariadb > values.yml
  config on demand
    config line 378 persistent.storageClass: "nfs-client" in values.yml   
  helm install hit-mysql bitnami/mariadb -f mysql.values
```
### Ref
- https://artifacthub.io/packages/helm/bitnami/mariadb