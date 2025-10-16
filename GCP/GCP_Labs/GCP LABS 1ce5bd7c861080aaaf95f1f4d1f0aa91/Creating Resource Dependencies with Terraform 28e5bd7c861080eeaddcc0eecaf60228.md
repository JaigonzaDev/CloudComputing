# Creating Resource Dependencies with Terraform

# **Overview**

In this lab, you will create two VMs in the default network. We will use variables to define the VM's attributes at runtime and use output values to print a few resource attributes.

We will then add a static IP address to the first VM to examine how terraform handles implicit dependencies. We will then create a GCS bucket by mentioning explicit dependency to the VM to examine how terraform handles explicit dependency.

# **Objectives**

In this lab, you learn how to perform the following tasks:

- Use variables and output values
- Observe implicit dependency
- Create explicit resource dependency