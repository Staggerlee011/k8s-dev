# confluence using rds and ebs

- to allow confluence to be resilient we need to use ebs for the confluence_home
- to allow confluence to be resilient and ha we will use rds instead of kube database

# steps

- create eks ([00-create-cluster](00-create-cluster/readme.md))
- create rds and connect to eks ([wordpress-rds](wordpress-rds/readme.md))
- run from this directory `kubectl apply -f .`

# updates

- update configmap.yaml `ATL_JDBC_URL` with the endpoint of the rds service
- 