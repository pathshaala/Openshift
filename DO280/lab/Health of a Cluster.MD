# Inspect Cluster

- login to Cluster

```
    oc login -u kubeadmin -p password https://api.ocp4.example.com:6443
```

- get nodes

```
    oc get nodes
```
```
    oc status
```
```
     oc get csr
```
```
    oc get co 
```
---
### CPU and memory from your nodes

```
    oc adm top nodes
```

- describe nodes

```
    oc describe node master01
```
---
### Node logs
```
oc adm node-logs master01
```
-u can be used as unit for logs, like kubelet, crio
```
oc adm node-logs -u kubelet master01
```
-- role for spacfic node role
```
oc adm node-logs --role master 
```
---
### Connect to node, debud mode
```
$ oc debug node/master1

# chroot /host
    - it will mount msater node to your local system.

# systemctl status kubelet
# systemctl status cri-o
# crictl ps --name openvswitch
# exit
# exit

``` 

---

### View logs of pod with 2 or more containers.
- list openshift-image-registry operators pods: below operator show 2/2 which means it has 2 container inside pod
```
    oc get pods -n openshift-image-registry
    NAME                                                READY   STATUS ...
    cluster-image-registry-operator-564bd5dd8f-s46bz    2/2     Running ...
    image-registry-794dfc7978-w7w69                     1/1     Running ...
```

```
oc get pods cluster-image-registry-operator-56b55fcd89-9z46h -n openshift-image-registry -o jsonpath={.spec.containers[*].name}
```
or
```
oc logs cluster-image-registry-operator-56b55fcd89-9z46h -n openshift-image-registry
```
- once u have container name use -c with container name
```
    oc logs --tail 3 cluster-image-registry-operator-56b55fcd89-9z46h -n openshift-image-registry -c cluster-image-registry-operator
```
