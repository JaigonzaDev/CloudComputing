# Kubernetes Engine (GKE)

Autopilot 

is **a mode of operation that simplifies cluster management by automating node configuration and management, allowing users to focus on their services and applications**

In Autopilot mode, Google manages the nodes and infrastructure, provisioning, configuring, and managing resources and hardware, including scaling.

This mode is designed to provide a hands-off approach to using Kubernetes on Google Cloud, reducing the need for node management operations and maximizing cluster efficiency.

https://cloud.google.com/kubernetes-engine/docs/resources/autopilot-standard-feature-comparison?hl=es-419

---

You are assigned to maintain a Google Kubernetes Engine (GKE) cluster named dev that was
deployed on Google Cloud. You want to manage the GKE configuration using the command line
interface (CLI). You have just downloaded and installed the Cloud SDK. You want to ensure that future
CLI commands by default address this specific cluster. What should you do?

A. Use the command gcloud config set container/cluster dev.
B. Use the command gcloud container clusters update dev.
C. Create a file called gke.default in the ~/.gcloud folder that contains the cluster name.
D. Create a file called defaults.json in the ~/.gcloud folder that contains the cluster name.

## Setting a default cluster for `gcloud`

To set a default cluster for `gcloud` commands, run the following command:

```
gcloud config set container/clusterCLUSTER_NAME
```

Replace **`CLUSTER_NAME`** with the name of your cluster.

---

You want to permanently delete a Pub/Sub topic managed by Config Connector in your Google Cloud project. What should you do?
A. Use kubect1 to delete the topic resource. 

B. Use gcloud CLI to delete the topic.
C. Use kubect1 to create the label deleted-by-cnrm and to change its value to true for the topic resource.
D. Use gcloud CLI to update the topic label managed-by-cnrm to false.

- **Config Connector** es una herramienta que permite **gestionar recursos de Google Cloud (como Pub/Sub topics, buckets, etc.) usando Kubernetes**.
- Cuando un recurso (como un **Pub/Sub topic**) **es administrado por Config Connector**, **NO debes borrarlo directamente con gcloud** ni desde la consola, porque **Config Connector lo recrearía** automáticamente basado en el estado deseado definido en Kubernetes.
- **¿Cómo debes eliminarlo entonces?** → **Debes borrar el recurso de Kubernetes** usando `kubectl delete`, ya que **Config Connector observa los recursos de Kubernetes** y al ver que el recurso fue eliminado, **borra también el recurso real en Google Cloud**.