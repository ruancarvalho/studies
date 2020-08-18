# Hands-On Microservices with Kubernetes

Book written by Gigi Sayfan

July 2019

## Introduction

## Getting Started with Microservices

### Programming in the small – less is more

Imagine a very simple program. 

There aren't any third-party dependencies. There is no IO (files, databases, network). There is no need for authentication or authorization. There is no need to rate limit calls. There is no logging, no metrics collection. There is no versioning, health checks, or configuration. There is no deployment to multiple environments and no monitoring in production.

Consider integrating this simple program into a big enterprise system.

The simplest operations of it might have cascading impacts.
And then there is a natural jump in complexity.

**The promise of microservices is that by following proper architectural guidelines and established patterns, the additional complexity can be neatly packaged and used across many small microservices that work together to accomplish the system goals.**

These services should be shielded from the encompassing system most of the time.

This takes a lot of effort to provide the right degree of isolation. Also, it needs testing and debugging in the context of the entire system.

### Making your microservice autonomous

To fight complexity make your microservice autonomous.

An autonomous service doesn't depend on other services in the system or third-party services. 

An autonomous service manages its own state and can be largely unaware of the rest of the system.

> **I like to think of autonomous microservices as similar to immutable functions.**

Autonomous services never change the state of other components in the system.

This way, its complexity remains the same, no matter how the system evolves and however it is being used by other services.

### Employing interfaces and contracts

Whenever you expose something as an interface, you can freely change the implementation behind it. 

Interfaces are a construct that's being used within a single process. 

Extremely useful for testing interactions with other components, which are plentiful in microservice-based systems.

