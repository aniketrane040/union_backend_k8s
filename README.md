# Setting up the Union Backend on Minikube

This guide will walk you through the steps to set up the Union Backend on a Minikube cluster.

## Prerequisites

Before you begin, make sure you have the following installed:

- Minikube: [Installation Guide](https://minikube.sigs.k8s.io/docs/start/)
- kubectl: [Installation Guide](https://kubernetes.io/docs/tasks/tools/)

## Ingress

In this I have defined only Ingress Resource for routing but there is no actualy Ingress Controller defined.
but As minikube has it's own builtin controller it wll work in minikube but on other kubernetes cluster such as eks, aks, etc..
