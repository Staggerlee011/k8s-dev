# Create cluster

Create a eks cluster based on a yaml file.

    NOTE: linux academy allows in us-east-1 and us-west-2

## create key for nodes

First you will need a key to manage the nodes:

    `aws ec2 create-key-pair --key-name eks-key`

## creation

Second create cluster by using yaml config file:

    `eksctl create cluster -f eks-cluster.yaml`

## post-install check

Post install check that kubectl works

    `kubectl get nodes`
