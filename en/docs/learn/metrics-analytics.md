# Integration insights

## Configuration

Integration metrics are published from WSO2 integration components as logs. Ballerina and MI components can be configured to publish these metrics logs as follows:

### Ballerina

Add the following line to the `Config.toml` file in the Ballerina project. If a `Config.toml` does not exists, create a new file in the same level as the `Ballerina.toml` file.

```
metricsLogsEnabled=true
```

### Micro Integrator

Add the following configuration to the `deployment.toml` file. 

```
[[synapse_handlers]]
name = "MetricsLogger"
class = "com.wso2.metrics.MetricsLogger"
```

Mount the updated `deployment.toml` file to `/home/wso2carbon/wso2mi-4.3.0/conf/deployment.toml` in MI pods.

## Integration insights dashboard

Integration insights dashboard displays insights derived from metrics collected from all integration deployments in the environment.

### Filtering panel

Filtering panel can be used to filter insights by deployment, entry point, time period, and by using custom queries.

<a href="{{base_path}}/assets/img/learn/metrics-filter.png"><img src="{{base_path}}/assets/img/learn/metrics-filter.png" alt="low-code" width="100%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Request count over time

Displays the request count over the selected time period. Request status (success or failure) is color coded in the bar chart.

<a href="{{base_path}}/assets/img/learn/request-count.png"><img src="{{base_path}}/assets/img/learn/request-count.png" alt="low-code" width="100%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Request count per API

Displays the number of requests received by each API in the environment. Successful and failed requests are color coded.

<a href="{{base_path}}/assets/img/learn/requests-per-api.png"><img src="{{base_path}}/assets/img/learn/requests-per-api.png" alt="low-code" width="80%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Response time per API

Displays the average reponse time of each API in the bar chart. 90th percentile reponse time of corresponding APIs are shown as a line chart.

<a href="{{base_path}}/assets/img/learn/response-times.png"><img src="{{base_path}}/assets/img/learn/response-times.png" alt="low-code" width="80%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Metrics table

Displays the request count and average response time for each entry point in the table format.

<a href="{{base_path}}/assets/img/learn/metrics-table.png"><img src="{{base_path}}/assets/img/learn/metrics-table.png" alt="low-code" width="100%" style="padding-top: 10px; display: block; margin: auto;" ></a>









