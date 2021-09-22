### Task

- Task is a collection of steps and step is a refrence of container.
- Step is a small operation in CI/CD flow e.g. run unit test
- Each step will have an image
- Basic unit in kubernete is Pod and Task creates pod
- Task help in grouping same logical steps and ordering of execution of steps as well
-

### Taskrun

- It initiate the execution of Task with specific input and output on the cluster
- Taskrun execute all steps of Task in same order asdefine in the Task
- It execute all steps untill successful or failure occures
