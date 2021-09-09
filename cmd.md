helm install --name my-release stable/mariadb -f values.yaml \
  --set rootUser.password=ROOT_PASSWORD \
  --set replication.password=REPLICATION_PASSWORD