---
layout: default
title: Not enough CPU resource
parent: Pod
nav_order: 2
---
# Not enough CPU resource
There can be many reason why a pod is in a Pending state.  One reason is that
the `pod` has requested more CPU than there is available in the cluster.

# How k8sbot can help
By asking k8sbot to describe the `pod`.  It will give you pertinent details on
why the pod is in a `pending` state.

## Command:
```
@k8sbot describe pod <pod name>
```

## Response:
```
NAME                                                                            READY     STATUS    RESTARTS  AGE       POD IP              NODE IP             
echoserver-init-not-enough-cpu-657f6fb8f5-wmgj5                                 ---       Pending   ---       ---```                                               
*Pod Conditions:*
```TYPE                STATUS    REASON              MESSAGE   
PodScheduled        False     Unschedulable       0/3 nodes are available: 3 Insufficient cpu.
```

*Events:*
```
TYPE      REASON              FROM                     MESSAGE   
Warning   FailedScheduling    default-scheduler        0/3 nodes are available: 3 Insufficient cpu.
```

*Recommendation:*
```
* The nodes available don't have enough cpu resources.  This usually means that the pod has requested for more CPU than is available on the cluster
```
