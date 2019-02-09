---
layout: default
title: No registry secret for a private image
parent: Pod
nav_order: 2
---
# No registry secret for a private image
There can be many reason why a pod is in a Pending state.  One reason is that
the `pod` is referencing a secret that does not exist.

# How k8sbot can help
By asking k8sbot to describe the `pod`.  It will give you pertinent details on
why the pod is in a `pending` state.

## Command:
```
@k8sbot describe pod <pod name>
```

## Response:

TBD
