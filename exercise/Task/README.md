## Task
---

### What is Task

---

Task is a collection of steps and steps are the reference of containers and run as a kubernetes pod on the cluster.
Each step runs in a separate container but within a single pod and shares pod resources and network among them.

### What is Step

---

Step is a smallest unit operation of CI/CD workflow e.g. build image,build binary,push the image to the registry.
Each step contains an image so it run in a separate container

### Why we need it

---

It is required to perform unit task e.g unit test in the CI/CD workflow which might have one or many steps

### Sample task

```
apiVersion: tekton.dev/v1beta1
kind: Task
metadata:
  name: first-task
spec:
  steps:
    - name: echo
      image: ubuntu
      command:
        - echo
      args:
        - 'Hello World'

```

## Taskrun

---

### What is TaskRun

---

Taskrun intiates the execution of the task and requires specific input and produces specific output.
These input and output are required by the Task defines in the Taskrun.
Task's input and output are customized.

It execute all steps of the task untill successful or failure occures.

### Taskrun sample
```
apiVersion: tekton.dev/v1beta1
kind: TaskRun
metadata:
  name: first-task-run
spec:
  taskRef:
    name: first-task

```
