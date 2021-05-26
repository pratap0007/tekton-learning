# Task

- Task is a collection of `steps` that you define and arrange in specific order of execution as part of your CI flow.
- Task execute as a pod in your kubernetes cluster
- Tasks are namespce scoped while cluster Tasks are cluster scoped

### Task Declaration

- Task declaration includes following elements
  1.  Paramter
  2.  Resources
  3.  Steps
  4.  Workspaces
  5.  Results

### Steps

- A step is a refrence to a container image that execute a specific tool on a specific input and prodeces a specific output
- To add steps to your task you will have to define steps filed(required) containing a list of desired steps
  - e.g.

```
	spec:
		steps:
			- name: step name
				resources:

```

-

### Configuring a task

A Task definition supports following fields

#### Required:

- apiVersion: speecify the apiVersion
- kind: Identify resources by kind e.g. `task`
- metadata: Specific metadata that uniqely identifies `Task` Resource object
- spec: Configuration information for `Task` resource object
- steps: Specifies one or more container images to run in the task

#### Optional

- `description`: Informative description of task
- `param`s`: Specifies execution parameter for task
- `workspace`s: Specifies the path to valumes required by the `task`
- `results`: specifies the name under whitch `Task` writes execution results
- `valumes`: specifies one or more valumes that will be available to to `steps` in task
- `stepTemplate`: Specifies a container step definition to use as basic for all `steps` in the tasks
- `sidecar`: Specifies Sidecar containers to run alongside the Steps in the Task
