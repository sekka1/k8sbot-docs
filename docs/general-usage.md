---
layout: default
title: General Usage
nav_order: 2
---

# Command:
```
@k8sbot help
```

# Response: 
```
I can help you out with various items on Kubernetes.  I only have read permission on your cluster which means I can only read items and cannot change anything on the cluster.  I can initially perform most "kubectl get" commands.

Usage:
    @k8sbot <command>

Feedback commands:
    feedback <your feedback here>
            - Dont forget to include your email if you want us to respond and any information you want us to see.  We do not save any of the information that flows through our system.
            - You can include anything in the message to use.  Code blocks, snippets, long for text, etc

Set Channel setting commands:
    set cluster <cluster-name>
    set namespace <namespace name>

Get commands:
    get cluster
    get namespace
    get pods
    get services (coming soon)
    get ingress

Pod commands:
    describe pod <pod name>

Service commands:
    trace service <service name> (coming soon)

Ingress commands:
    trace ingress <ingress name>

Deployment commands:
    trace deployment <deployment name> (coming soon)

Use "@k8sbot <command> --help" for more information about a given command.
```
