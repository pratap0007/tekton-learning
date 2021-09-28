### Cluster Task

---

### What is Cluster Task

---

Cluster task is a special kind of task which scoped entire cluster.Basically it help in managaing cluster level operation.

### Why do we need it

---

Suppose some task required by many projects under different name space so in that case need to create only one Cluster task

### Sample of ClusterTask

```
apiVersion: tekton.dev/v1beta1
kind: ClusterTask
metadata:
  name: hello-clustertask
spec:
  steps:
    - name: step-1
      image: alpine
      script: |
        #! /bin/bash
        echo "hello clustertask"
```
