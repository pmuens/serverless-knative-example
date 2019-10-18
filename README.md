# Serverless Knative Example

Example on how to use the [Knative provider plugin](https://github.com/serverless/serverless-knative) for the [Serverless Framework](https://github.com/serverless/serverless) to deploy Knative workloads on [Kubernetes](https://kubernetes.io) clusters.

## Prerequisits

- [Google Cloud SDK](https://cloud.google.com/sdk/) on your local machine
- [Node.js](https://nodejs.org/en/) >= 8 on your local machine
- [Docker](https://www.docker.com) in your local machine
- [Kubernetes Cluster](https://kubernetes.io) e.g. on the [Google Cloud Platform](https://cloud.google.com) (or your local machine)
- [Knative](https://knative.dev) on your Kubernetes Cluster

## Knative installation

Follow [this tutorial](https://github.com/meteatamel/knative-tutorial/tree/5ac77498c5715775c8ed4c114bc1bee7ac09554e#installation) if you need to install Knative on your Kubernetes cluster.

## Quickstart

1. Run `serverless install --url https://github.com/pmuens/serverless-knative-example`
1. Run `cd serverless-knative-example`
1. Run `npm install`
1. Create a `docker-creds.json` file in the root of this project and add your Docker Hub credentials (see below for file structure)
1. Generate a [`kubeconfig`](https://rancher.com/docs/rancher/v2.x/en/cluster-admin/kubeconfig/) file (follow this tutorial if you use the [Google Cloud Platform](https://cloud.google.com/kubernetes-engine/docs/how-to/cluster-access-for-kubectl#generate_kubeconfig_entry))
1. Run `serverless deploy`
1. Run `serverless invoke -f helloWorld`
1. Run `serverless remove`

## `docker-creds.json`

```json
{
  "username": "jdoe",
  "password": "S0M3P455W0RD"
}
```
