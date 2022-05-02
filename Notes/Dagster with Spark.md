---
title: "Dagster with Spark"
created-at: "2022-05-01 19:55"
public: true
language: en
tags: [idea]
---

# Dagster with Spark

## Working with Java

- The JVM stdout and stderr are not piped, so error is present in the console, but not in the Dagit, because it is not added to the exception raised in the Python code.
	- https://github.com/apache/spark/blob/master/python/pyspark/java_gateway.py#L87

## Working with Spark standalone deployment

- It's not possible to set deploy mode to `cluster` when using PySpark. So the application driver is always run locally.
	- If Spark is deployed on a host in VPN, you must specify the driver host, so the workers (inside VPN) can communicate back to the driver (outside VPN). By default the driver will send IP address in its network, which will (or only may?) be different than IP address assigned within VPN. How to find the address of your local host within the VPN you can SSH into the remote machine and check the SSH connections. For details see [[SSH]]. Set the driver IP address with `spark.driver.host` and `spark.driver.bindAddress` - these allows using a different address from the local one. A good explanation of the problem and solution: https://stackoverflow.com/a/59208883.
- [Spark documentation: Spark standalone](https://spark.apache.org/docs/latest/spark-standalone.html)
- https://becominghuman.ai/real-world-python-workloads-on-spark-standalone-clusters-2246346c7040
	- I didn't read it completely.
	- It contains some of the solutions I've figured out.

## Related

[[Apache Spark]]
