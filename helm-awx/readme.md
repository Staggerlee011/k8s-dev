# helm awx install

install ansible awx following: https://www.jeffgeerling.com/blog/2019/run-ansible-tower-or-awx-kubernetes-or-openshift-tower-operator

## steps

`kubectl apply -f https://raw.githubusercontent.com/geerlingguy/tower-operator/master/deploy/tower-operator.yaml`

`kubectl create namespace tower`

`Kubectl config set-context --current --namespace=tower`

`kubectl apply -f tower.yaml`

    NOTE: enabled loadbalncer on tower_hostname

`Kubectl get pods`
