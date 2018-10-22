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

# Go Nexus *

Working with a variety of developers we think that we should be agnostic to languages the contributors and projects want to use. 

AURA is being built in [Go](https://golang.io) with (Nexus)[https://github.com/gammazero/nexus]. This router is the main manager of communication for the services of various components that comprise the corpus of the project. The router provides endpoints that provide the connecting applications with realms. Each realm is comprised of topics that can be subscribed and published to using a PubSub paradigm. This decouples the components from each other and unifies the API into a one-to-many pattern.

![Overview Diagram for Access 2 Justice Application](/images/a2j-application-overview-diagram.jpg)

# We Are Currently Working To An Alpha Build

The aim of this utility is to manage the messages and payloads that are communicated back and forth from an eclectic range of components and modules. The goal is to reduce complexity for the developers of these components and the need to learn new code stacks to contribute. 
