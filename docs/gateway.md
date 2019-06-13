# Gateway


## Overview
A maven vertx gateway application that aggregates API calls to backend services by providing a condensed REST API for front-end.

## Dependencies

It requires following things to be installed:

* Java: ^8.0.
* Maven

## Deployment strategy

### Local deployment

This section provides step by step guidelines on how to run the application:

* To run the application use the command given below:

```bash
clean package vertx:run
```

### Helm Charts

If you have configured helm on your cluster, you can deploy gateway microservice using our generic `Application` chart from our public chart repository and deploy it via helm using below mentioned commands

Note:
The default values are placed inside [values.yaml](deployment/values.yaml]).

```bash
helm repo add stakater https://stakater.github.io/stakater-charts

helm repo update

helm install --name gateway --namespace nordmart-store stakater/application -f deployment/values.yaml
```