# simplified way to run kube-bench

Run the kube-bench job on a Pod in your Cluster pulling the image from dockerhub:

    `kubectl apply -f job-eks.yaml`

Find the Pod that was created, it should be in the default namespace:

    `kubectl get pods --all-namespaces`

Retrieve the value of this Pod and output the report, note the Pod name will vary:

    `kubectl logs kube-bench-<value>`

You can save the report for later reference:

    `kubectl logs kube-bench-<value> > kube-bench-report.txt`
