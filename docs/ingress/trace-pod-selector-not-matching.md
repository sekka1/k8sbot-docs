---
layout: default
title: Trace - Service port not matching pod port
parent: Ingress
nav_order: 2
---
# Trace - Service port not matching any pod label selectors
There can be many things wrong with an ingress and why it does not work.  One
problem can be that the `service` label selecting the `pod` is incorrect or is not
able to find any pod(s) with those labels current.  This means that there are no
endpoints for this service which means the `service` will not be able to route
traffic to any destination.

# How k8sbot can help
By asking k8sbot to trace out an `ingress` it will follow all of the mappings and
let you know if it finds anything wrong.

## Command:
```
@k8sbot trace ingress <ingress name>
```

## Response:
```
Ingress
======

External
--------
Address: xxxx

Annotations:
kubernetes.io/ingress.class: kong-gar

Host                Path                Backend             Service                       Pod                                                         
----                ----                -------             ========                      ===                                                         
                                                                 Port                Target    Endpoints           IP/Pod Name    Port(s)        
                                                                 ----                ------    ---------           -----------    -------        
trace-ingress-3.ingress.com
                    /                   trace-ingress-3:80       http 80/TCP         8080/TCP                                                    
                    /admin              trace-ingress-3:9090     admin 9090/TCP      9090/TCP
```                                                    
Recommendations:
```
* There are no endpoints/pods associated with the service.  This means that there are no pods to route the ingress to.
* The service selector label(s) could be incorrect.
* There could be no pods with this service selector label(s) running.
```
