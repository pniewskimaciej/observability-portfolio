# Telecom Data & Custom Feeds

Examples of custom network-data feeds and integrations designed and implemented using data collected by NETSCOUT probes.

These projects demonstrate how raw network data can be transformed into **customer-specific information feeds** and integrated with downstream platforms and business systems.

The use cases cover different network interfaces, User Plane and signaling data, data filtering, enrichment and streaming integration.

> **Note:** All public examples are anonymized or synthetic. No customer-sensitive information is included.

---

## Use Cases

### Use Case 01 – User Plane URL Intelligence

A custom User Plane feed designed to identify subscribers accessing predefined URLs, including competitor price-plan pages.

The selected records were exported to the customer's external Apache Kafka broker for further processing.

[View Use Case →](./use-case-01-url-intelligence/)

---

### Use Case 02 – Location-Based Marketing

A custom feed based on S1-MME and SGs data containing subscriber and cell-location information.

The feed was exported to the customer's Kafka environment and used as an input to downstream location-based marketing processes.

[View Use Case →](./use-case-02-location-marketing/)

---

## Technologies

`NETSCOUT Probes` · `Apache Kafka` · `JSON` · `Avro` · `Python` · `Bash` · `Linux` · `REST APIs`

---

## Skills Demonstrated

**Network Data Engineering · Custom Feed Design · Data Transformation · Data Enrichment · Kafka Integration · Telecom Analytics · Solution Design · Requirements Analysis**
