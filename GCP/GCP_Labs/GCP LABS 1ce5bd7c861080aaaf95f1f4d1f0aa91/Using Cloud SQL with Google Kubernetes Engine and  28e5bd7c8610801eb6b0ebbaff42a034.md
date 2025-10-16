# Using Cloud SQL with Google Kubernetes Engine and Workload Identity

# **Overview**

In this lab, you set up a Kubernetes Deployment of WordPress connected to Cloud SQL via the SQL Proxy. The SQL Proxy lets you interact with a Cloud SQL instance as if it were installed locally (localhost:3306), and even though you are on an unsecured port locally, the SQL Proxy makes sure you are secure over the wire to your Cloud SQL Instance.

To complete this lab you'll create several components. First you create a GKE cluster, next you create a Cloud SQL Instance to connect to, and a Service Account to provide permission for your Pods to access the Cloud SQL Instance, this will be authenticated using Workload Identity. Finally you deploy WordPress on your GKE cluster, with the SQL Proxy as a Sidecar, connected to your Cloud SQL Instance.

# **Objectives**

In this lab, you learn how to perform the following tasks:

- Create a Cloud SQL instance and database for Wordpress.
- Create credentials and Kubernetes Secrets for application authentication.
- Configure Workload Identity.
- Configure a Deployment with a Wordpress image to use SQL Proxy.
- Install SQL Proxy as a sidecar container and use it to provide SSL access to a CloudSQL instance external to the GKE Cluster.