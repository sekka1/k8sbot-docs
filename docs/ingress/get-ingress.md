---
layout: default
title: Get Ingress
parent: Ingress
nav_order: 1
---
# Get Ingress
Get ingress returns a list of ingresses in the current namespace.

## Command:
```
@k8sbot get ingress
```

## Response:
```
NAME                                    HOSTS                                   ADDRESS             PORTS          AGE            
trace-ingress-1                         trace.ingress.com                                           80                            
trace-ingress-2                         trace-ingress-2.ingress.com                                 80,9090                       
trace-ingress-3                         trace-ingress-3.ingress.com                                 80,9090                       
trace-ingress-4                         trace-ingress-4.ingress.com                                 80,9090  
```
