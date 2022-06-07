In general Dagster uses the `workspace.yaml` file to find repositories with jobs. The repositories can be defined as local files, local or published packages, or [[gRPC]] servers. Dagster includes such gRPC server.

The trick with separate deployment of the Dagster and Dagit from the user code is that the Dagster deployment defines all user code deployments as repositories available through gRPC server. Where, the user code deployments must run this server.

The issue is that Dagster does not offer any kind of auto-discovery or any kind of automated attachment of newly deployed user code to an existing Dagster instance. Adding new gRPC server requires modifying of the `workspace.yaml` defined with the [[Kubernetes config map]] resource and attached to the Dagster deployment.

It can be done by searching for specific labels, generating the `workspace.yaml` configuration and updating the config map.

---

[[Dagster]]
[[Dagster deployment on Kubernetes]]
[[Kubernetes]]
