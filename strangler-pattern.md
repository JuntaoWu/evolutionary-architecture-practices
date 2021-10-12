---
description: Strangling a monolith
---

# Strangler Pattern

The process of transforming large legacy monoliths into decoupled, scalable microservices systems is more complex than can be imagined.

Monoliths are easy to deploy and can have a good performance because of the usage of shared memory. Still there are several reasons to move away from this way of working to a microservices approach:

* if the application has evolved into a big ball of mud
* tight coupling forces you to test and deploy the whole application when adding features
* when the application has become too large and too complex to be able to do automated regression tests
* when starting up the application becomes very slow
