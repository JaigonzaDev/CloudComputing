# Hello Cloud Run

# **Overview**

[Cloud Run Logo](https://cdn.qwiklabs.com/1d2sNybCwEWoWfxc%2FNEUFPsGq9ntjZEQgOgq2RJHmE4%3D)

[Cloud Run](https://cloud.google.com/run) is a managed compute platform that enables you to run stateless containers that are invocable via HTTP requests. Cloud Run is serverless: it abstracts away all infrastructure management, so you can focus on what matters most — building great applications.

[Cloud Run](https://cloud.google.com/run) is built from [Knative](https://cloud.google.com/knative/), letting you choose to run your containers either fully managed with Cloud Run, or in your [Google Kubernetes Engine](https://cloud.google.com/kubernetes) cluster with Cloud Run on GKE.

The goal of this lab is for you to build a simple containerized application image and deploy it to Cloud Run.

# Objectives

In this lab, you learn to:

- Enable the Cloud Run API.
- Create a simple Node.js application that can be deployed as a serverless, stateless container.
- Containerize your application and upload to Artifact Registry.
- Deploy a containerized application on Cloud Run.
- Delete unneeded images to avoid incurring extra storage charges.