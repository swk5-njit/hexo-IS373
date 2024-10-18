---
title: Containerization
date: 2024-10-17 20:50:08
---
# Containerization
Containerization refers to using containers in running a program/content management system. Even though the two sound similar, there are differences between a container and a virtual machine, and there are also different situations where one of the two would be more effective as opposed to the other.

![Containerization](https://github.com/dfianuale/IS373/blob/main/graphics/c1.jpg)

## What is a Container and how does it work?
A container is an isolated software component that runs on top of an operating system's kernel and is separate from other containers, that contains applications and some OS APIs. They also contain all libraries or dependencies that are required by those applications. Unlike virtual machines (VMs), all containers on a single machine will share that machine's kernel, making them more portable than a VM. Despite sharing a kernel, having the containers separate allows for more consistent and efficient use, since programs running in different containers will not affect one another. They are also more lightweight than a VM, since they do not contain their own kernel but instead run on that of the operating system (or VM, containers can run inside VMs). Containers can also be scaled up or down depending on the applications being run, and their requirements.

## Benefits of using containers
* Containerized applications are portable between opposing physical machines or a cloud, and they can be run from anywhere, provided they are run from the container itself.
* Containerized apps are more resource-efficient than VMs, meaning they use less resources overall and distribute used resources more effectively than a virtual machine.
* Isolating containers from both the host machine and each other offers improved security.
* Developers can integrate with DevOps environments and manage containers at scale more easily using Kubernetes.
* Both virtualized environments or bare-metal servers can be used.
* Applications start up fast and can be scaled easily.

## Docker
![Docker](https://github.com/dfianuale/IS373/blob/main/graphics/c2.png)
Docker is a program for Windows, Linux, and Mac that allows users to create their own localized containers, which can then be used to develop, ship, and run applications. It is one of the most popular alongside Kubernetes.

## Key Docker Terms
* "Container" in this context refers to an active instance of Docker and the application(s) contained in that instance.
* A Docker image is a read-only template that contains the code for the application and any dependencies or libraries it requires.
* A Dockerfile is a text file that tells the user how to build an instance of Docker.
* The Docker desktop app gives access to the Docker Hub, which is a space where users can publicly share Docker images for applications they have developed.

## Installing Docker
Any user can download and install the Docker desktop app from its website at <docker.com>. Install instructions for Windows, Linux, and Mac users can be found at <docs.docker.com/engine/install>.  The install process will depend on your operating system.

\* Windows users will need to install the Windows Subsystem for Linux (WSL2). Click [here](https://learn.microsoft.com/en-us/windows/wsl/install) to learn more about WSL2. \*

## Docker Commands
Users can run these commands using bash (on Linux or through WSL2) or the Command Prompt (Windows).
To run a container:

> docker run hello-world

List running containers

> docker ps (add "-a" to list all containers, not just those currently running)

To stop a running container:

> docker stop [container id] (replace "stop" with "rm" to remove the container entirely)

To remove a Docker image:

> docker rmi [image id]

Sources:
* <https://learn.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm>
* <https://www.geeksforgeeks.org/virtualization-vs-containerization/>
* ChatGPT
* https://www.ibm.com/blog/the-benefits-of-containerization-and-what-it-means-for-you/
