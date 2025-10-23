---
title: Concept Guides
layout: default
nav_order: 2
parent: Docs
has_children: true
permalink: /docs/concepts/
---

## Why Technical Writers Need to Understand Docker and Kubernetes

Technical writers produce documentation that helps users deploy and operate software. They must understand **Docker** and **Kubernetes** because these technologies define how modern applications run. This knowledge ensures the documentation is precise, actionable, and relevant to the technical audience.

***

### 1. Documenting Core Deployment Procedures Accurately

The deployment process for most modern software relies on container technology. Writers must master container concepts to create accurate guides.

* **Containers and Images:** The writer explains how to use **Docker images** to package an application and its dependencies. They document commands like `docker pull` to fetch the image and `docker run` to start the container.
* **Orchestration:** When the application is complex (microservices), **Kubernetes** manages the containers. The technical writer details how users write or apply **YAML manifest files** (e.g., Deployments, Services) to configure the cluster. The writer clearly describes Kubernetes components like **Pods**, **Nodes**, and **Namespaces**.
* **Configuration:** The writer documents how users pass environment settings to the application using Kubernetes objects, such as **ConfigMaps** and **Secrets**.

***

### 2. Streamlining Communication with Engineers

Understanding the terminology of containerization and orchestration improves the writer's efficiency when working with Subject Matter Experts (SMEs).

* **Effective Inquiry:** The writer asks specific questions about resource allocation, persistent storage (**Volumes**), and network connectivity (**Services**). This precision reduces ambiguity and the need for repetitive Q\&A sessions.
* **Translating Concepts:** The writer correctly interprets technical feedback about deployment strategies (e.g., Blue/Green, Canary releases) and translates these complex engineering discussions into simple, clear documentation.

***

### 3. Validating Documentation Directly

To ensure the setup instructions work correctly, the technical writer must be able to test them.

* **Local Verification:** The writer uses tools like **Docker Desktop** or local Kubernetes environments (e.g., **Minikube** or **k3s**). This hands-on practice allows the writer to verify every command, confirm the application starts successfully, and capture accurate screenshots of the process.
* **Testing Prerequisites:** The writer identifies all necessary prerequisites, such as installing the `kubectl` command-line tool or configuring a registry, and documents these steps clearly before the main deployment procedures.

In summary, the technical writer **writes** about the platform, **speaks** the platform's language, and **tests** the application on the platform. Docker and Kubernetes are the technical platforms of today.