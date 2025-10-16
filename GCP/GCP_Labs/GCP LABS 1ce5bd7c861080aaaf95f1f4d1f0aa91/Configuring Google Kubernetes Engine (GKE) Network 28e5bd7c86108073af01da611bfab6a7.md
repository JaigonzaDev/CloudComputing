# Configuring Google Kubernetes Engine (GKE) Networking

# **Overview**

In this lab, you will create a standard cluster which uses internal RFC 1918 IP addresses, add an authorized network for API access to it, and then configure a network policy for Pod security.

**Note:** For this lab, GKE Standard Mode will be used. The lab explores cluster network policies and these are enabled by default in GKE Autopilot.

# Objectives

In this lab, you learn how to perform the following tasks:

- Create and test a standard cluster which uses internal RFC 1918 IP addresses.
- Configure a cluster for authorized network control plane access.
- Configure a Cluster network policy.