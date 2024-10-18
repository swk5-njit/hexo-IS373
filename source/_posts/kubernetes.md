---
title: Kubernetes
---

# Kubernetes
Kubernetes is a platform that developers can use to manage containers and containerized workspaces at a large scale. It was made open-source by Google in 2014, and it has a vast ecosystem with various tools, utilities, etc.

## How does Kubernetes work?
Unlike Docker, Kubernetes is more focused on managing containers at scale, instead of focusing on one or two at a time. Kubernetes provides an application programming interface (API) that controls where and how containers run. It schedules containers to run in virtual machines based on resource availability and requirements. Containers are organized into units called "pods", which users can then scale up and down to fit their needs. Kubernetes can also scale pods automatically, as well as managing resource allocation, balancing workloads, and monitoring the health status of resources and allowing apps to restart or replicate as needed, among other functions.

## The benefits of Kubernetes
* Kubernetes can be used to make applications portable, since they run separately from their infrastructure in containers. This means they can be moved between machines or to a cloud while remaining consistently functional.
* Containerized applications can then be run across a cluster of servers, or multiple clusters of servers, with Kubernetes scaling them automatically to maintain the health of each container. Users can also scale their containers manually with a command.
* Kubernetes has a vast community of users who have made tools and utilities to add more functions to Kubernetes, such as security and monitoring functions.
* Users can give Kubernetes nodes to run containerized tasks in, and specify how much CPU and memory each one can needs. From there, the platform can allocate resources automatically to make the most effective use of them. 
* The platform automatically maintains container health by restarting containers that fail and killing any containers that do not respond to user-defined health checks.
* DevOps practices such as CI/CD, infrastructure as code, and constant monitoring can be employed in Kubernetes environments, which allows one to keep up with the speed at which their application grows, moving fast in a changing environment.

## Before Kubernetes...
Before virtualization and containerization came to be, applications ran on physical servers. This was difficult to manage because physical servers at the time could not automatically allocate resources, which led to management issues. For example, one application would end up using most of the resources on its respective server, severely impacting the performance of other applications that ran on that server. While one solution to this problem would have been to run every application on a different physical server, this would not have worked out, since resources would go unused, and the organization in question would have to spend a lot of money to maintain that many servers. 

Now, virtualization allows both individual users and organizations to emulate physical servers, which costs less and is easier to maintain, especially with Kubernetes. Kubernetes also prevents underutilization of resources by allocating resources to where they are most needed, increasing functionality without diminishing the performance of other applications in the same virtual machine. Containers can also run inside a virtual machine, providing another layer of security and ease of management and access.

## Kubernetes versus Docker
The biggest difference between these two entities is the scale at which they are used. While Docker is most often used to develop containerized applications at a personal level or to publish onto the Docker Hub, Kubernetes is used to manage clusters of containers at a much larger scale. Additionally, while Docker is used to create and run containers, Kubernetes is more oriented towards managing those containers. Finally, the main benefit of Kubernetes is that complex applications can be defined and run at scale, while Docker is beneficial for standardizing operations and shipping code quickly.

Sources:

* https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-kubernetes/?msockid=0ea882de80cc69ce01fc92c0813168e7#watch-how-kubernetes-works
* https://kubernetes.io/docs/concepts/overview/