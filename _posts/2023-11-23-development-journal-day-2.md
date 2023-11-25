# Access vCluster via kubeconfig

According to the [vCluster documentation](https://www.vcluster.com/docs/using-vclusters/access), An Ingress Controller](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/) with SSL passthrough support will provide the best user experience.

In reconciling the vCluster instance custom resource, we also create an ingress resource for the vCluster. The ingress resource is annotated with the vCluster instance name. The ingress controller can use this annotation to route traffic to the correct vCluster.