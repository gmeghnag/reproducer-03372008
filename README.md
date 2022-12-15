# reproducer-03372008

## How-To
- Create the `reproducer-03372008` [Namespace](https://raw.githubusercontent.com/gmeghnag/reproducer-03372008/main/namespace.yaml) with the required annotations for pruning `pipelinerun` and `taskrun`, also the `hello-world` [Task](https://raw.githubusercontent.com/gmeghnag/reproducer-03372008/main/task.yaml) and `hello-world-pipeline` [Pipeline](https://raw.githubusercontent.com/gmeghnag/reproducer-03372008/main/pipeline.yaml) by executing the following command:
```
oc apply -k https://github.com/gmeghnag/reproducer-03372008
```
- Then, start the pipeline in the `reproducer-03372008` namespace, either manually from the console or using `tkn` cli:
```
tkn pipeline start -n reproducer-03372008 hello-world-pipeline --showlog
```
- Wait for 3 minutes, you shoud see the `TaskRun` and `PipelineRun` being pruned.


## Environment

Tested on version:
```
OCP 4.9.52
openshift-pipelines-operator-rh.v1.6.4
```
