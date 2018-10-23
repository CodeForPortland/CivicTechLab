+++
title = "AURA: An Agnostic Query"
description = "Developing a microservice architecture to unify contribution tech stacks."
tags = ["AURA", "Development", "Blog"]
date = "2018-10-21"
location = "Tigard, OR"
slug = "AgnosticQueries"
type = "post"
author = "Rex Beatie"
+++

# AURA.*

Working with a variety of developers we think that we should be agnostic to the languages that the contributors and projects use. 

**AURA** is that solution, it stands for an **A**gnostic **U**tility for **R**emote **A**pplications. It's purpose is to provide polygoltism to the contribution tech stack. 
Basically it's a design pattern used primarily in large scale application delivery systems known as a microservice architecture. 
The idea behind it is to decouple the components and modules to provide an orthogonal development environment so that those working on back and front end 
do not have to worry about how the other developers create the solutions they are working on, they only need to understand how to send and receive data from them. 

It is our intent to generalize, document and teach this process to allow it to be used as is, for any project that finds it's facilitation useful to promote
a better developing experience and to provide a better quality of deployment for a product. We have a prometheus mind set a want to bring the fire of enterprise to civic infrastructure.

In short, the goal is to reduce the size and complexity for developers on the application layer and the need to learn new code stacks to work cohesively. 

# An Overview

AURA has two main *features* and two *constraints*. 

## Features

The two main developments are the focus for the **Civic Tech Lab** team. They will provide a secure framework and user friendly API for other developers to achieve their goals.

- **The Router** - We are building in [Go](https://golang.io) with [Nexus](https://github.com/gammazero/nexus). 
    This router is the main manager of communication for the services of various components that comprise the corpus a project. 
    The router provides [WAMP v2](https://wamp-proto.org) protocol endpoints that provide the connecting applications within **realms**. 
    Each *realm* is comprised of **topics** that can be **subscribed** and **published** too, using a **PubSub** pattern. 
    This decouples the components from each other and unifies the API into a **one-to-many** pattern.

- **Kubernetes and Helm** - Using [Kubernetes (K8S)](https://kubernetes.io) can connect each component in a scalable and resilient SWARM pattern. *K8S* which is also in *Go*, 
    gives us the ability to keep instances of *contributions* in a controlled state of communication with other *services* and *components* and further decouples each of which in **pods** that can be replicated. 
    [Helm](https://helm.sh) is *K8s*'s dependency manager and it's configuration files would be how a team would adapt this project to fit with their own.  


## Constraints

The are two required components for facilitating a service or front-end module to be able to be used by this framework. 
Ideally the **Civic Tech Lab** team would also provide working examples that a developer could just cut and paste straight into their code.

- **Dockerfiles** - *Containerization* is the process of creating an environment for your application, an analogy for a container
   is a baby computer inside of another computer. This is a core piece to decoupling tech stacks and ensuring that a program can run on any system. 
   To achieve this we are using [Dockerfiles](https://www.docker.com/get-started) and these would need to be placed inside each components root directory.
   
- **WAMP v2** - `WAMP != WAMP` [WAMP](https://wamp-proto.org) stands for Web Application Message Protocol, and it is a standard for communication over **websockets**.
    Think of WAMP as HTTP for a websocket. HTTP is a standard, it comes with predefined features like **message codes** eg `404` and `200` or **methods**, eg `GET`, `POST`. 
    WAMP contains it's own *message codes* eg `8` (**ERROR**) and methods eg, `SUBSCRIBE` and `PUBLISH`. 

  
# We Are Currently Working To An Alpha Build

Check it out @ [Github](https://github.com/CodeForPortland/CivicTechLab-AURA) or if you like to contribute send a message to [Rex](rex@codeforpdx.org) or just 
<a class="github-button" href="https://github.com/CodeForPortland/Civic-Tech-Lab-AURA/fork" data-icon="octicon-repo-forked" aria-label="Fork CodeForPortland/Civic-Tech-Lab-AURA on GitHub">Fork</a> us! :)
<!-- Place this tag in your head or just before your close body tag. -->
<script async defer src="https://buttons.github.io/buttons.js"></script>
 
