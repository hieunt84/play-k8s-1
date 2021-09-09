### Command kubectl
```console
k get pod -w
k get storageclass
k get pvc
k logs services-db-mariadb-primary-0 -f
k scale sts/my-release-mariadb-secondary --replicas=2
```
### Command helm
```console
helm install my-release bitnami/mariadb -f values.yaml
```