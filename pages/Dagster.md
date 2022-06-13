---
tags: [technology]
---

## General info

[Home](https://dagster.io/)
[Documentation](https://docs.dagster.io/)

## Issues and solutions

### Execution logs

The job run in console failed, but there was no error details.

By default, the job execution logs are stored in the `${DAGSTER_HOME}/storage/<run_id>/compute_logs/` directory.

The [documentation describes how to configure the storage for compute logs](https://docs.dagster.io/deployment/dagster-instance#compute-log-storage) (how Dagster names them). The configuration should be used for Dagster being deployed on cloud infrastructure using containers, so the the logs are not lost when a container exits.
