helm install my-release stable/mariadb -f values.yml \
  --set rootUser.password=ROOT_PASSWORD \
  --set replication.password=REPLICATION_PASSWORD