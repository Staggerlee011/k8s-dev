# wordpress-rds

install wordpress using a rds mysql instance.

## steps

- create eks cluster
- create rds cluster
- create vpc peering between
- update routing tables on each to allow connections from the other
- update security group for rds to allow from eks range
- update mysql-service with dns of rds instance
- apply mysql-service `kubectl apply -f mysql-service.yaml`
- apply wordpress.yaml `kubectl apply -f wordpress.yaml`

## basic test of rds

run busy box in interactive mode:

`kubectl run -i --rm --tty debug --image=busybox --restart=Never -- sh`

run nc in busy box:

`nc mysql-service 3306`

exit busybox with exit

`exit`

## connect to wordpress

run kubectl to find external load balancer address

`kubectl get service wordpress`

connect to external-ip plus port ie:

`a8c2870a95ff511ea81350eaa4044251-1247372896.us-east-1.elb.amazonaws.com:30052`
