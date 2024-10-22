# Learning-Kubernetes-Essentials


## KubeConfig Overview

A `kubeconfig` file is a configuration file used to manage access to Kubernetes clusters. It helps you interact with clusters by specifying how you can connect to them, including user credentials and cluster details.

When working with Kubernetes, `kubectl` (the command-line tool) uses this file to know which cluster to connect to and how to authenticate the request.

### What Does a KubeConfig File Do?

- It helps Kubernetes tools (like `kubectl`) connect to a Kubernetes cluster.
- It specifies the cluster's API endpoint, authentication details, and the user profile to use.
- It allows you to switch between different clusters and user contexts easily.

### Main Components of a KubeConfig File:

1. **Clusters**: Information about the Kubernetes clusters you can connect to. This includes the name of the cluster and the API server URL.
2. **Users**: Authentication details such as certificates, tokens, or usernames and passwords used to access the clusters.
3. **Contexts**: A combination of a cluster, a user and a namespace , so you can specify which user is interacting with which cluster.

Each section defines essential pieces of information to ensure that your Kubernetes commands are sent to the correct cluster with the right access permissions.

### How it Works

When you run a `kubectl` command, it checks the `kubeconfig` file to determine which cluster to talk to and which user credentials to use. By specifying different contexts, you can quickly switch between clusters or user roles without having to reconfigure everything each time.

## Difference Between Kubernetes Objects and Resources

### Kubernetes Objects
A **Kubernetes Object** is something you create in the Kubernetes system to describe what you want to happen in your cluster. These objects represent the desired state, such as running applications, setting configurations, or managing storage.

#### Examples of Kubernetes Objects:
- **Pods**: Run one or more containers.
- **Deployments**: Manage Pods and ensure their desired state.
- **Services**: Expose your application to the network.
- **ConfigMaps**: Store configuration data.

Think of an object as **what** you're telling Kubernetes to create or manage.

---

### Kubernetes Resources
A **Kubernetes Resource** refers to the API endpoint used to interact with these objects. It’s the path or URL that Kubernetes uses to manage and track the objects in the system. You use resources to **create, update, delete, or view** Kubernetes objects.

#### Examples of API Resources:
- `/api/v1/pods`: Interact with Pod objects.
- `/api/v1/deployments`: Interact with Deployment objects.
- `/api/v1/services`: Manage Service objects.

Think of a resource as **how** you interact with Kubernetes objects through the API.

---
