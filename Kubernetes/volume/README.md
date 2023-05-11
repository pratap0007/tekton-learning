## Create a valume and  mount in the Pod
In kubernetes, a volume is a storage abstraction that provides a way for container to 
store and access data. It can be though of as a directory within container's file system 
that has a lifecycle indepnedant of the container.

To craete the persistent volume claim in kubernetes, you can follow these steps



### pv vs pvc
---
PV represents a piece of storage in the cluster, it can be though of as a logical
representation of a physical storage device, such as disk and network share.
manage and created by the administrator of cluster 

on the other hand pvc is a request for a specific amount of storage from a pv,
it is a resource that a user creates to request to storage from the cluster.
A pvc is bound to a single pv and provides a way for a user to access a piece of storage that is 
managed by the cluster.



----
- LOcal Node type: emptyDir,hostPath, local
- Distributed file system type: gulsterfs, cephfs
- Special type: persistent volume, persistent volume claim 
- Cloud provider type : Vsphere, Cinder


## how to assign a single volume to specific container pod
--
- Assign by the volume mount 