# Kubernetes Exercise: Deploying an Nginx Pod

This repository contains a Kubernetes exercise completed for the Nautilus DevOps team, focusing on deploying a pod with Nginx. Here's a detailed explanation of the task and the commands used.

## Task Overview

The Nautilus DevOps team is practicing deploying pods and services on the Kubernetes platform. The specific task was to:

- Create a pod named `pod-nginx` using the `nginx:latest` image.
- Set the label `app` to `nginx_app`.
- Name the container `nginx-container`.

Note that the `kubectl` utility has been configured to work with the Kubernetes cluster on `jump_host`.

## Steps and Explanation

1. **Inspecting the Current Namespace and Pods**:
   ```
   kubectl get namespace
   kubectl get pods
   ```
   These commands are used to check the existing namespaces and pods in the Kubernetes cluster.

2. **Creating a YAML File for the Pod Configuration**:
   ```
   vi /tmp/pod.yaml
   ```
   A YAML file was created to define the pod's configuration. Here's the content of the file:

   ```yaml
   apiVersion: v1
   kind: Pod
   metadata:
     name: pod-nginx
     labels:
       app: nginx_app
   spec:
     containers:
     - name: nginx-container
       image: nginx:latest
   ```
   Please note that the provided code snippet in the task has the wrong pod name and label; it's corrected here.

3. **Creating the Pod**:
   ```
   kubectl create -f /tmp/pod.yaml
   ```
   This command reads the YAML file created earlier and deploys the pod according to the configuration.

4. **Verifying the Pod Creation**:
   ```
   kubectl get pods
   ```
   This final command verifies that the pod has been created and is running as expected.

## Conclusion

This exercise demonstrates a typical workflow for deploying a simple pod using Kubernetes. It encompasses various essential commands and provides hands-on experience in managing Kubernetes resources.

---
