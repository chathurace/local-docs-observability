The architecture of the observability solution is shown below.

<a href="{{base_path}}/assets/img/architecture/observability_architecture_m2.png"><img src="{{base_path}}/assets/img/architecture/observability_architecture_m2.png" alt="low-code" width="80%" style="padding-top: 10px; display: block; margin: auto;" ></a>

Fluent Bit pods are deployed as a Kubernetes DaemonSet. Therefore, One Fluent Bit pod will be deployed in each VM in the Kubernetes cluster. These Fluent Bit pods capture logs emitted by all pods in their corresponding VMs and send those to OpenSearch data pods. Before sending logs, Fluent Bit pods perform some preprocessing operations such as extracting required fields, adding metadata fields, and renaming fields.

Each MI and Ballerina pod sends tracing data to Data Prepper according to the Open Telemetry format. Data Prepper performs some preprocessing operations and sends processed tracing data to OpenSearch data pods.

OpenSearch data pods handle all data processing operations such as indexing, searching, and aggregations. OpenSearch master pods perform cluster coordination operations such as index/shard allocations and maintaining the cluster's health. OpenSearch dashboard pods act as the backend for the observability dashboard. All log visualizations and dashboards are deployed into dashboard pods. 