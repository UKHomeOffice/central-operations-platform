# Integrating a service with Prometheus Client and SysDig

There are a few parts for ensuring that your service can communicate with Prometheus. The technical service requirements created by ACP: https://github.com/UKHomeOffice/technical-service-requirements give a little guidance to three endpoints you should provide in your application

## Prerequisites

From the ACP [monitoring and metrics document](https://github.com/UKHomeOffice/technical-service-requirements/blob/master/docs/monitoring_metrics.md) you can see that each service needs to provide three endpoints:
- `/metrics` endpoint for your service to expose all necessary metrics
- `/healthz` endpoint for the liveness Probe
- `/readiness` endpoint for the readiness probe


So, using your service, as long as you provide the three above endpoints, you can integrate with SysDig.

## Example of integrating Prometheus Client and SysDig in a node service

In node, we can use [express-prometheus-middleware](https://www.npmjs.com/package/express-prometheus-middleware) in order to set an endpoint for `/metrics` with some default metric collection happening. Other languages are covered with some links at the bottom of this document.

The default metrics collected are from using: https://github.com/siimon/prom-client

We do not need to have a Prometheus instance running in order to use the client, we can simply use the client on its own.
```javascript
expressApplication.use(prometheusMiddleware({
    prefix: 'prefix_metrics_',
    metricsPath: '/metrics',
    collectDefaultMetrics: true,
    requestDurationBuckets: [0.1, 0.5, 1, 1.5],
}));
```

## Deployment

In the Kubernetes deployment scripts, we need to provide some annotations to let the SysDig agent know about the endpoint, and that it can start collecting metrics from the microservice. An example can be found here: https://gitlab.digital.homeoffice.gov.uk/cop/form-api-server-deploy/blob/master/kube/deployment.yml

```yaml
template:
  metadata:
    labels:
      name: "{{.API_NAME}}"
    annotations:
      prometheus.io/scrape: 'true'
      prometheus.io/port: "{{.API_PORT}}"
```

## Other use cases

There are many ways you can create and track metrics using the prom-client – using counters to track how often events are happening (say a 500 error) or using a histogram to track the size and frequency of events, for example you could use Histogram to create a timer for how long a certain event takes (like a request to a service). More details are available here: https://github.com/siimon/prom-client

## Other languages

Client libraries in other languages:

If you would like to use another client library, please check the list here: https://prometheus.io/docs/instrumenting/clientlibs/

There is a python client here: https://github.com/prometheus/client_python
