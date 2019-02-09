---
layout: default
title: Trace - Service port not matching pod port
parent: Ingress
nav_order: 2
---
# Trace - Service port not matching pod port
There can be many things wrong with an ingress and why it does not work.  One
problem can be that the `service` port specified does not match what is set
in the `pod`.  This would lead not being able to reach your pod's service via
this ingress.

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
trace-ingress-4.ingress.com
                    /                   trace-ingress-4:80       http 80/TCP         8888/TCP                                                    
                                                                                                                   trace-ingress-4-5db9d55849-8w7qs               
                                                                                               10.44.21.6:8888     10.44.21.6                    
                                                                                                                                  http 8080/TCP  
                                                                                                                                  admin 9090/TCP
                    /admin              trace-ingress-4:9090     admin 9090/TCP      9090/TCP                                                    
                                                                                                                   trace-ingress-4-5db9d55849-8w7qs               
                                                                                               10.44.21.6:9090     10.44.21.6                    
                                                                                                                                  http 8080/TCP  
                                                                                                                                  admin 9090/TCP
```
Recommendations:
```
* The service target port does not match up with a port specified in the pod.
* The target service port is 8888/TCP but the pod doesnt have this port spedified.
```
