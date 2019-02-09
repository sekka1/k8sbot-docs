---
layout: default
title: Send Us Feedback
nav_order: 3
---
# Feedback

We are always looking for feedback if our k8sbot has given you helpful information.
At anytime you can send us feedback via telling k8sbot:

```
@k8sbot feedback <your feedback here>
```

* Include your email address if you want us to email you back about it.
* Include any information you want us to have.  We do not keep any information going through the bot

## Example:

```
@k8sbot feedback This was ingress tracing was very useful

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
