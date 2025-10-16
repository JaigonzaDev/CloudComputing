# Automating the Deployment of Infrastructure Using Terraform

# **Overview**

Terraform enables you to safely and predictably create, change, and improve infrastructure. It is an open-source tool that codifies APIs into declarative configuration files that can be shared among team members, treated as code, edited, reviewed, and versioned.

In this lab, you create a Terraform configuration with a module to automate the deployment of Google Cloud infrastructure. Specifically, you deploy one auto mode network with a firewall rule and two VM instances, as shown in this diagram:

[Terraform configuration diagram](https://cdn.qwiklabs.com/tQ3NS2xpirSs1UXVcklIYVQM7WkUc%2F8iC7ryGFPSfRs%3D)

# Objectives

In this lab, you learn how to perform the following tasks:

- Create a configuration for an auto mode network
- Create a configuration for a firewall rule
- Create a module for VM instances
- Create and deploy a configuration
- Verify the deployment of a configuration