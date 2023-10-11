# IN261 - Gain a Comprehensive View of Event-Driven Architecture

![Pic 1](/./images/IN261-1.jpeg)

## Description

An event-driven architecture is a software architecture using events as the core means for interaction between its software components. This includes capture, communication, processing, and persistence of events.  Event-driven architectures represent an architectural approach and aren’t based on a specific programming language.

Event-driven architectures are a great fit for distributed software environments and enable minimal coupling. A defining element of an event-driven architecture is that event producers don’t know which event consumers listen for an event and, to go beyond this, what the consequences of the event on the consumer side are. Parties interested in receiving events can subscribe to published events at will. This might result in not only a loose coupling but also a highly flexible software architecture that is constantly changing and adjusting.

In this session we will get a broad understanding of EDAs in an SAP context. 

## Overview

SAP Integration Suite, advanced event mesh is a fully managed event streaming and management service that enables enterprise-wide and enterprise-grade event-driven architecture. It complements SAP Event Mesh for more demanding scenarios and is a full blown, general purpose Event Mesh. AEM offers enterprise-grade performance, reliability, security and governance. It scales to very large use cases – and very means very very very in this case.

![Pic 1](/./images/IN261-2.png)

This session allows you to get an end-to-end impression of event-driven architecture hands-on. Starting from the event source, you will follow the flow of outbound events via the event broker to the event consumer.

As an event source we will use SAP S/4HANA Cloud and SAP S/4HANA. SAP Integration Suite, advanced event mesh will be our event broker, and events are consumed by an HTML/JS based event consumer.

The session will be broad rather than deep, with the goal to provide a highspeed end-to-end experience, with a specific focus on our new event broker SAP Integration Suite, advanced event mesh.

You will be able to experience basic and advanced features of SAP Integration Suite, advanced event mesh.

During the free flow part towards the end you can use the HTML/JS based event consumer and an HTML/JS based event producer to try out different features of SAP Integration Suite, advanced event mesh.

Features touched, some just shortly, some in more detail, include:

- SAP S/4HANA Cloud standard notification events
- SAP S/4HANA Event-Enablement Add-On Events
- SAP Business Accelerator Hub
- SAP Integration Suite, advanced event mesh queues
- SAP Integration Suite, advanced event mesh Cluster Manager
- SAP Integration Suite, advanced event mesh Mesh Manager
- SAP Integration Suite, advanced event mesh Event Designer and Event Management
- SAP Integration Suite, advanced event mesh Try Me!

## Requirements

- Understanding the basics of event-driven architectures, namely events, queues, topics, event subscriptions ...
- You would be able to execute most of the excercises without prior experience by just following the descriptions. For taking value out of the chance to explore the brokers, specifically Advanced Event Mesh, some experience with event-driven architectures is recommended.

## Exercises

![Pic 1](/./images/IN261-3.png)

Provide the exercise content here directly in README.md using [markdown](https://guides.github.com/features/mastering-markdown/) and linking to the specific exercise pages, below is an example.

- [Getting Started](exercises/ex0/)
- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)

 ## User Data and Password 

Your user data and number can be found here.

In order to log into Advanced Event Mesh, you will use the email address. The password for Advanced Event Mesh will be provided by the moderators. 

 ## Background Material 

A lot of material to get up to speed with SAP Integration Suite, advanced event mesh is available.

- Blogs

    - [SAPs Event-Driven Ecosystem](https://blogs.sap.com/2022/09/01/saps-event-driven-ecosystem-revisited/)
    - [Advanced Event Mesh](https://blogs.sap.com/2022/10/28/turn-your-erp-into-a-team-player-introducing-sap-integration-suite-advanced-event-mesh/ )
    - [SAP Event Mesh and Advanced Event Mesh](https://blogs.sap.com/2022/10/03/sap-integration-suite-advanced-event-mesh-vis-a-vis-sap-event-mesh-and-sap-integration-suite./)

- Videos

    - [Discover Event-driven Integrations](https://www.youtube.com/watch?v=r9lyC_2ss2U)
    - [SAP on Azure](https://www.youtube.com/watch?v=NNrzXbX3mk0)

- Documentation

    - [Help](https://help.pubsub.em.services.cloud.sap/Cloud/cloud-lp.htm)

## License
Copyright (c) 2023 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
