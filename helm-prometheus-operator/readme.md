# prometheus-operator

install prometheus operator using helm, it is a pre-configured prometheus, grafana and alerting.

## chart

https://github.com/helm/charts/tree/master/stable/prometheus-operator

## install guide

ensure helm is up to date:

`helm update`

install via helm (NOTE: V3 of helm has removed --name by the looks of it and errors trying to use simply remove the --name to run like below)

`helm install monitoring stable/prometheus-operator`

    installs into default.. tried using --namespace but errors.

after install edit the service for grafana to put the networking to LoadBalancer.

`kubectl edit -n default service/monitoring-grafana`
