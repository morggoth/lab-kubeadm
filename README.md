# Creating a cluster with Kubeadm

Here I try to install K8S cluster with help of [this tutorial](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/).

## How to start the lab

```bash
vagrant up
vagrant ssh node1

# Use --pod-network-cidr flag, if you want to use Flannel
# https://github.com/coreos/flannel/blob/master/Documentation/kubernetes.md
kubeadm init --pod-network-cidr=10.244.0.0/16
```

## How to stop the lab

```bash
vagrant destroy -f
```