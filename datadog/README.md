# Datadog – DNS & LDAP Monitoring

## Overview

An end-to-end observability solution for monitoring DNS and LDAP services, combining infrastructure health, service-level KPIs, logs, application traces and geographic analysis.

Test data collected and processed by NETSCOUT probes was stored in Kafka and streamed into Datadog through a Logstash processing pipeline.

---

## Data Pipeline

```text
NETSCOUT Probes
      │
      ▼
Processed Test Data
      │
      ▼
Kafka Topic
      │
      ▼
Logstash
      │
      ├── GeoIP enrichment
      ├── Timestamp transformation
      └── Data processing
      │
      ▼
Datadog
      │
      ▼
Dashboards · Logs · Traces
```

---

## Dashboard

![Datadog DNS and LDAP Monitoring](./datadog-dns-ldap-monitoring.png)

> **Note:** The dashboard screenshot has been anonymized and contains no customer-sensitive or confidential information.

---

## Use Case

The dashboard was designed to provide a **single operational view of DNS and LDAP service health**, combining infrastructure, service performance and detailed troubleshooting information.

The dashboard is divided into three main sections.

### 1. Infrastructure Health

Provides an overview of the underlying DNS and LDAP server health, including:

* RAM utilization
* Disk utilization
* Partition usage
* Network-related KPIs
* Server health indicators

This section provides the infrastructure context required when investigating service degradation.

### 2. DNS & LDAP Service KPIs

Focuses on the actual performance and availability of the services:

* Response time
* Failure rate
* Failure trends
* Worst clients affected by failures
* Servers with the highest response times
* Service performance trends

This allows technical teams to identify degraded services and determine which clients or servers are most affected.

### 3. Logs, Traces & Geographic Analysis

Provides deeper troubleshooting capabilities through:

* Server logs
* Application traces
* Failure analysis
* Geographic distribution of affected traffic
* Regional failure-rate analysis

The geographic view helps correlate service failures with the location of affected users or traffic.

---

## Logstash Processing

Logstash was used as the integration and processing layer between Kafka and Datadog.

As part of the pipeline, I addressed several data-processing requirements:

### GeoIP Enrichment

I enabled GeoIP enrichment for **server IP addresses**, allowing the data to be analyzed geographically in Datadog.

### Timestamp Transformation

The source data did not use the required timestamp format by default. I implemented timestamp transformation in Logstash to convert the timestamps into **ISO 8601 format** before sending the data to Datadog.

### Kafka Integration

Logstash subscribed to the relevant Kafka topic containing test data collected and processed by NETSCOUT probes and forwarded the processed data to Datadog.

---

## My Contribution

I designed and implemented the monitoring solution across the data pipeline and observability layer, including:

* Consuming test data from Kafka using Logstash
* Troubleshooting and resolving data-processing issues
* Implementing GeoIP enrichment
* Transforming timestamps into ISO 8601 format
* Forwarding processed data to Datadog
* Designing the DNS and LDAP monitoring dashboard
* Defining infrastructure and service-level KPIs
* Creating views for logs and application traces
* Adding geographic analysis of service failures
* Designing the dashboard for both operational monitoring and troubleshooting

---

## Technologies

**Data Collection**

`NETSCOUT Probes`

**Data Streaming**

`Apache Kafka`

**Data Processing & Integration**

`Logstash`

**Observability**

`Datadog`

**Data Enrichment**

`GeoIP`

**Services**

`DNS` · `LDAP`

**Monitoring**

`Infrastructure Metrics` · `Logs` · `Traces` · `Service KPIs`

---

## Skills Demonstrated

**Observability · Data Pipelines · Kafka · Logstash · Datadog · Infrastructure Monitoring · Service Monitoring · Log Analysis · Application Tracing · GeoIP Enrichment · Troubleshooting · Dashboard Design**
