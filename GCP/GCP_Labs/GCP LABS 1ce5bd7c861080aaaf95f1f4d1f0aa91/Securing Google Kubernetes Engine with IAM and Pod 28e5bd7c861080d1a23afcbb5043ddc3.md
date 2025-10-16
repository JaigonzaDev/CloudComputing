# Securing Google Kubernetes Engine with IAM and Pod Security Admission

# **Overview**

You will control access to GKE clusters using IAM. You will create a pod security policy to restrict privileged Pod creation, and you will test that policy. You will also perform IP address and credential rotation.

**Note:** For this lab, GKE Standard Mode will be used. The lab expores Pod Security Policies and it is not possible to create policies that override the built-in security settings in GKE Autopilot.

# **Objectives**

In this lab, you learn how to perform the following tasks:

- Use IAM to control GKE access
- Create and use Pod security policies to control Pod creation
- Perform IP address and credential rotation

**Note:** For this lab, Google Cloud Skills Boost has provisioned you with two user names available in the Connection Details dialog.
In this lab, we will refer to these accounts as **Username 1** and **Username 2**.