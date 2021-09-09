helm install my-release stable/mariadb -f values-production.yaml \
  --set rootUser.password=ROOT_PASSWORD \
  --set replication.password=REPLICATION_PASSWORD