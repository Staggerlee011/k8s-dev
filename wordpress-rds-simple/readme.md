# wordpress using rds simple

removing the service that connects to rds

## steps

- create eks cluster
- create rds cluster
- vpc peering
- routing table update on ecah vpc
- update security group for rds to connect to eks
- update wordpress.yaml WORDPRESS_DB_HOST

## basic test of rds

run busy box in interactive mode:

`kubectl run -i --rm --tty debug --image=busybox --restart=Never -- sh`

run nc in busy box:

`nc <database endpoint> 3306`

exit busybox with exit

`exit`
