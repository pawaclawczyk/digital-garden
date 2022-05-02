---
title: "Apache Spark working with AWS S3"
created-at: "2022-05-02 21:33"
public: true
language: en
tags: [idea]
---

# Apache Spark working with AWS S3

The capability to work with AWS S3 is provided by the `hadoop-aws` library.

The library is not included by default add it in `spark.jars.packages` configuration option as `org.apache.hadoop:hadoop-aws:3.3.1`. Use version respective for your Hadoop version.

All [configuration options](https://hadoop.apache.org/docs/stable/hadoop-aws/tools/hadoop-aws/index.html#General_S3A_Client_configuration) for the `hadoop-aws` can be configured in the Hadoop configuration files or passed in Spark configuration with prefix `spark.hadoop.`, e.g.  `fs.s3a.endpoint` becomes `spark.hadoop.fs.s3a.endpoint`.

To provide path to data in an S3 bucket use `s3a://` protocol (not `s3://`), e.g. `s3a://bucket/path/to/data`.

[Spark documentation](https://spark.apache.org/docs/latest/cloud-integration.html) has information about Apache Spark working with cloud object stores.

## Related

[[Apache Spark]]
