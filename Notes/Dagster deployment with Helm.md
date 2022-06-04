---
title: "Dagster deployment with Helm"
created-at: "2022-05-24 17:21"
public: true
language: en
tags: [idea]
---

# Dagster deployment with Helm

I want to have a Dagster instance run on a [[Kubernetes]] cluster, on which I could run jobs from various projects, without the need to deploy a dedicated for each of them.

[Official documentation: Deploying Dagster with Helm](https://docs.dagster.io/deployment/guides/kubernetes/deploying-with-helm)


>The run worker jobs and pods are not automatically deleted, so that users are able to inspect results. It is up to the user to periodically delete old jobs and pods.


## First attempt

- follow the tutorial skip the minio part, there is a job that can be executed within a single pod, no data exchange is needed
- the data exchange is needed if ops are run in separate pods, I didn't test that
- the chart with very little configuration works 

The dagster chart deploys the two main services: Dagster daemon and Dagit. The first is responsible for 
There are:
- two system deployments:
	- Dagster daemon
	- Dagit
- one optional system deployment:
	- PostgreSQL
- two user deployments:
	- run worker
	- user code

```shell
helm repo add dagster https://dagster-io.github.io/helm

helm show values dagster/dagster > values.yaml

helm upgrade --install <deployment name> dagster/dagster -f <path to values>
```

