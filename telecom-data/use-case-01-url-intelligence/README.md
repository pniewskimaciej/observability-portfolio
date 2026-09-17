# Use Case 01 – User Plane URL Intelligence Feed

## Business Objective

The customer wanted to identify subscribers who were accessing **competitor price-plan pages** while using the customer's mobile network.

The objective was to provide this information to a downstream analytics or customer-engagement platform so that the operator could better understand customer behavior and use the information in its own business processes.

---

## Solution

I designed a custom **User Plane data feed** based on traffic collected by NETSCOUT probes.

Only traffic matching a predefined set of URLs was selected for export. The URLs represented competitor websites and specific pages related to their mobile price plans.

The resulting records were exported to the customer's **external Apache Kafka broker** for further processing.

---

## Data Flow

```text
Customer Network Traffic
          │
          ▼
   NETSCOUT Probes
          │
          ▼
     User Plane Data
          │
          ▼
   URL-based Filtering
          │
          │  Selected competitor
          │  price-plan URLs
          ▼
   Custom Data Feed
          │
          ▼
 External Kafka Broker
          │
          ▼
 Customer Analytics / Business Systems
```

---

## Feed Content

The feed contained subscriber and traffic-related information such as:

* IMSI
* MSISDN
* Timestamp
* Requested URL
* Traffic / session information
* Additional network dimensions required by the customer

Only records matching the customer's defined URL criteria were exported.

---

## My Contribution

I was responsible for designing the feed according to the customer's requirements, including:

* Understanding the business use case and required data
* Identifying the relevant User Plane data available from NETSCOUT probes
* Defining the filtering criteria
* Designing the feed structure and required fields
* Implementing URL-based selection logic
* Preparing the data for external Kafka delivery
* Supporting integration and validation with the customer's Kafka environment
* Troubleshooting the feed during implementation

---

## Technical Architecture

**Data Source**

`NETSCOUT Probes` · `User Plane Traffic`

**Filtering**

`URL-based Traffic Selection`

**Output**

`Custom Data Feed`

**Integration**

`Apache Kafka`

**Downstream Use**

`Customer Analytics` · `Business Intelligence`

---

## Skills Demonstrated

**User Plane Analytics · Network Data Engineering · Custom Feed Design · Traffic Filtering · Kafka Integration · Telecom Data · Requirements Analysis · Data Transformation · Solution Design**

---

## Sample Data

A synthetic example of the feed structure is provided in:

`sample-feed.json`

> **Important:** The sample contains fictional subscriber identifiers, URLs and values. It does not represent actual customer data.
