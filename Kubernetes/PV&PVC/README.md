## PV ( Persistent Volume)

---

- Kubernetes makes physical storage devices like your SSDs, NVMe disks, NAS, NFS servers available to your cluster in the form of objects called -- Persistent

---

- Each of these Persistent Volumes is consumed by a Kubernetes Pod (or Pods) by issuing a PersistentVolumeClaim object -- a PVC. A PVC object lets pods use storage from Persistent Volumes.


### Storage class
---
- A storageclass is a Kubernetes object that stores information about creating a persistent volume for your pod. With a storageclass, you do not need to create a persistent volume separately before claiming it.

-

## PVC (Persistent Volume Claim)

---
