# Analyzing integration logs

## Configuration

Log entries printed to the standard output or standard error by any pod in the environment will be captured by the observability solution. Ballerina components by default print all logs to the standard output. Micro Integrator only prints application logs to the standard output. Therefore, if it is necessary to access other Micro Integrator log types such as access logs and audit logs, it is necessary to associate the corresponding console appender with the required log type.

For example, if it is necessary to view MI HTTP access logs from the observability solution, uncomment the `logger.PassThroughAccess.appenderRef.HTTP_ACCESS_CONSOLE.ref = HTTP_ACCESS_CONSOLE` line in the `log4j2.properties` file. Once this is uncommented, PassThroughAccess logger configuration would look like this:

```
logger.PassThroughAccess.name = org.apache.synapse.transport.http.access.logs
logger.PassThroughAccess.level = DEBUG
logger.PassThroughAccess.appenderRef.HTTP_ACCESS_LOGFILE.ref = HTTP_ACCESS_LOGFILE
logger.PassThroughAccess.appenderRef.HTTP_ACCESS_CONSOLE.ref = HTTP_ACCESS_CONSOLE
logger.PassThroughAccess.additivity = false
```

Once the `log4j2.propertied` file is updated, it needs to be mounted to `/home/wso2carbon/wso2mi-4.3.0/conf/log4j2.properties` of Micro Integrator pods.

## Log analytics dashboard

### Logs over time

Views logs printed by all integration components over the selected time period.

<a href="{{base_path}}/assets/img/learn/log-over-time.png"><img src="{{base_path}}/assets/img/learn/log-over-time.png" alt="low-code" width="100%" style="padding-top: 10px" ></a>

### Logs by deployment

An environment can have multiple integration component deployments. For example, there can be two MI clusters and four Ballerina applications. This dashboard item shows logs printed by each of such integration component deployment.

<a href="{{base_path}}/assets/img/learn/logs-by-app.png"><img src="{{base_path}}/assets/img/learn/logs-by-app.png" alt="low-code" width="80%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Logs by entry point

Integrations can be triggered by many entry points such as an API call, GraphQL invocation, Kafka message, or manual activation. This dashboard item shows logs grouped under such entry points across the whole environment.

<a href="{{base_path}}/assets/img/learn/logs-by-trigger.png"><img src="{{base_path}}/assets/img/learn/logs-by-trigger.png" alt="low-code" width="80%" style="padding-top: 10px; display: block; margin: auto;" ></a>

### Log details

Individual log entries printed during the selected time period are displayed in this dashboard item. All details of any log entry can be viewed by clicking on the expand sign `>` in the left hand side.

<a href="{{base_path}}/assets/img/learn/logs.png"><img src="{{base_path}}/assets/img/learn/logs.png" alt="low-code" width="100%" style="padding-top: 10px; display: block; margin: auto;" ></a>
