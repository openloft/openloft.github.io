# We Need Templates & Instances for vCluster

To provision vClusters in a declarative manner, we need to define templates and instances for vClusters. This is similar to [Virtual Machine Classes for Tanzu Kubernetes Clusters](https://docs.vmware.com/en/VMware-vSphere/7.0/vmware-vsphere-with-tanzu/GUID-7351EEFF-4EF0-468F-A19B-6CEA40983D3D.html) and [AWS EC2 instance types](https://aws.amazon.com/ec2/instance-types/).

We reuse the [vCluster API](https://github.com/loft-sh/api) as the CRD for vCluster templates and instances. Each vCluster instance references a vCluster template. The [OpenLoft](https://github.com/openloft/openloft) (yet another K8s Operator) watches for vCluster instances and creates the corresponding vClusters.