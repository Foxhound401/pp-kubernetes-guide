
## Core Concepts

kubernetes.io > Documentation > Reference > kubectl CLI > [kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

kubernetes.io > Documentation > Tasks > Monitoring, Logging, and Debugging > [Get a Shell to a Running Container](https://kubernetes.io/docs/tasks/debug-application-cluster/get-shell-running-container/)

kubernetes.io > Documentation > Tasks > Access Applications in a Cluster > [Configure Access to Multiple Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/)

kubernetes.io > Documentation > Tasks > Access Applications in a Cluster > [Accessing Clusters](https://kubernetes.io/docs/tasks/access-application-cluster/access-cluster/) using API

kubernetes.io > Documentation > Tasks > Access Applications in a Cluster > [Use Port Forwarding to Access Applications in a Cluster](https://kubernetes.io/docs/tasks/access-application-cluster/port-forward-access-application-cluster/)

### List all nodes in the clusters

```bash
kubectl get nodes
```

<details><summary>output</summary>
<p>

```bash
~ via ⬢ v18.7.0 ➜ took 33s k get nodes
NAME                                          STATUS     ROLES    AGE     VERSION
ip-10-20-10-222.eu-west-1.compute.internal    Ready      <none>   11d     v1.19.6-eks-49a6c0
ip-10-20-10-45.eu-west-1.compute.internal     Ready      <none>   7d15h   v1.19.6-eks-49a6c0
ip-10-20-128-156.eu-west-1.compute.internal   Ready      <none>   18m     v1.19.15-eks-9c63c4
ip-10-20-128-241.eu-west-1.compute.internal   Ready      <none>   83m     v1.19.15-eks-9c63c4
ip-10-20-128-61.eu-west-1.compute.internal    Ready      <none>   15m     v1.19.15-eks-9c63c4
ip-10-20-129-71.eu-west-1.compute.internal    Ready      <none>   3h23m   v1.19.15-eks-9c63c4
ip-10-20-129-96.eu-west-1.compute.internal    Ready      <none>   24d     v1.19.15-eks-9c63c4
...
```

</p>
</details>

### Create a namespace called 'mynamespace' and a pod with image nginx called nginx on this namespace

```bash
kubectl create namespace mynamespace
kubectl run nginx --image=nginx -n mynamespace
```

<details><summary>output</summary>
<p>

```bash
namespace/mynamespace created
kubectl create namespace mynamespace
kubectl run nginx --image=nginx -n mynamespace
```
</p>
</details>


### Create deployment with image nginx called nginx on created namespace with 3 replicas

```bash
kubectl create deployment --image=nginx -n mynamespace --replicas=3 --port=80
```

<details><summary>output</summary>
<p>

```bash
deployment.apps/nginx-deployment created
```


</p>
</details>

