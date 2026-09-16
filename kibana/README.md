# Elasticsearch / Logstash / Kibana – HTTP & HTTPS Traffic Analytics

## Overview

This use case demonstrates an end-to-end pipeline for analyzing HTTP and HTTPS traffic using data generated from a customer-provided PCAP file.
The PCAP was replayed through NETSCOUT probes to produce network traffic data, which was then processed, enriched and indexed for analysis in Elasticsearch.

## Data Pipeline

Customer PCAP
     │
     ▼
NETSCOUT Probes
     │
     ▼
Network Traffic Data
     │
     ▼
Logstash
     │
     ├── ASN enrichment – Client IP
     ├── AS Path enrichment – Client IP
     ├── ASN enrichment – Server IP
     └── AS Path enrichment – Server IP
     │
     ▼
Elasticsearch
     │
     ▼
Kibana
     │
     ▼
Dashboards & Visualizations
```

## Objective

Create an analytical view of HTTP and HTTPS traffic that combines application-level information with network and Internet routing data.
The goal was to allow technical teams to understand **what applications and URLs were generating traffic, where the traffic was coming from and going to, and how it was distributed across networks and autonomous systems.**

## Data Enrichment

A key part of the solution was enriching the traffic data with Internet routing information.
Using Logstash, I enriched both **client and server IP addresses** with:

* ASN number
* AS Path

This allowed traffic to be analyzed not only by IP address, but also by the associated Autonomous System and routing path.

## Kibana Dashboards

The enriched data was loaded into Elasticsearch and used to create Kibana visualizations covering:

* Application traffic
* URLs
* SNI / Server Name Indication
* Traffic volume
* Client ASN
* Client AS Path
* Server ASN
* Server AS Path
* Traffic distribution and trends

This provided the ability to correlate application and URL activity with the underlying network and Internet infrastructure.

## My Contribution

I designed and implemented the complete data analysis workflow, including:

* Processing a customer-provided PCAP through NETSCOUT probes
* Defining the required data and enrichment workflow
* Designing Logstash processing and enrichment
* Mapping client and server IP addresses to ASN and AS Path
* Loading the enriched data into Elasticsearch
* Designing Kibana visualizations and dashboards
* Defining KPIs and analytical views for HTTP/HTTPS traffic
* Correlating application-level and network-level information

## Technologies

**Data Collection:**
NETSCOUT Probes · PCAP

**Data Processing:**
Logstash

**Data Storage & Search:**
Elasticsearch

**Visualization & Analytics:**
Kibana

**Data:**
HTTP · HTTPS · SNI · IP · ASN · AS Path

## Skills Demonstrated

**Network Traffic Analysis · Data Engineering · Logstash Pipelines · Elasticsearch · Kibana · Data Enrichment · Network Intelligence · Data Visualization · Telecom Analytics**
