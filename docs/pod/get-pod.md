---
layout: default
title: Get Pod
parent: Pod
nav_order: 1
---
# Get Pod
Get pod returns a list of pods in the current namespace.

## Command:
```
@k8sbot get pod
```

## Response:
```
NAME                                                                            READY     STATUS    RESTARTS  AGE       POD IP    NODE IP             
echoserver-init-not-enough-cpu-657f6fb8f5-wmgj5                                 ---       Pending   ---       ---       ---       ---                 
echoserver-not-enough-cpu-677d7fd76c-9nwg2                                      ---       Pending   ---       ---       ---       ---                 
echoserver-not-enough-cpu-memory-554ccbc779-8pp28                               ---       Pending   ---       ---       ---       ---                 
echoserver-not-enough-memory-5ff579854d-v2twq                                   ---       Pending   ---       ---       ---       ---                 
echoserver-running-state-dd88b69c6-ts8rm                                        ---       Running   ---       ---       ---       ---                 
trace-ingress-1-86df888956-dkgtm                                                ---       Running   ---       ---       ---       ---                 
trace-ingress-2-8468885857-pgp26                                                ---       Running   ---       ---       ---       ---                 
trace-ingress-3-56d7cc6ff9-jzgpk                                                ---       Running   ---       ---       ---       ---                 
trace-ingress-4-5db9d55849-wqxjw                                                ---       Running   ---       ---       ---       ---     
```
