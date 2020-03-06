# efs 4 eks

steps to create a efs and use it as storage for eks.

These are steps based on using efs-provisioner: https://aws.amazon.com/premiumsupport/knowledge-center/eks-pods-efs/

## create efs storage

manual create efs storage and use the k8s nodes subnets

    update configmap with region / efs id
    update deployment with dns name of efs

```
kubectl apply -f class.yaml
kubectl apply -f configmap.yaml
kubectl apply -f rbac.yaml
kubectl apply -f deployment.yaml
kubectl apply -f claim.yaml
kubectl apply -f test-pod.yaml
```