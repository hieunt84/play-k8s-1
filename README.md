# play-k8s-1
### Deploy mysql using persistent volume
```console
   config persistent in mysql.values
     ref from line 320
   helm repo add bitnami https://charts.bitnami.com/bitnami
   helm install -f mysql.values hit-mysql bitnami/mysql
```
### Ref
- https://artifacthub.io/packages/helm/bitnami/mysql