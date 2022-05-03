---
title: "Technology Journal"
created-at: "2022-05-03 11:58"
public: true
language: en
tags: [journal]
---

# Technology Journal

- Tuesday 2022-17-03 17:17:01 
	- #dagster #kubernetes 
	- #todo Deploy Dagster on Kubernetes.
		- How to release new or updated jobs?
		- How to integrate jobs from multiple projects?

- Tuesday 2022-05-03 13:48:04 
	- #kubernetes #apache-spark #minio
	- #todo Configure gateway service on Kubernetes to MinIO and Spark installed outside the cluster.

- Tuesday 2022-05-03 13:08:57 
	- #apache-spark #spark-driver #spark-remote
	- The run on remote Spark takes a lot of time.
	- #todo Test if there is communication between driver on localhost and MinIO API. Use [[ufw - uncomplicated firewall]] to block traffic between machines.
	- #todo Test if it works faster without MinIO.

- Tuesday 2022-05-03 12:56:40 
	- #apache-spark #spark-driver
	- #remember to export `SPARK_HOME` when running driver on localhost, otherwise the configuration for event log is not loaded, so there will be no entry in history server.

- Tuesday 2022-05-03 12:11:34 
	- #apache-spark #spark-standalone
	- #todo I must check how are the jobs on Spark run when core and memory limits are applied to spark application.
	- #todo I must check what happens if I start many workers in a standalone Spark installation.
