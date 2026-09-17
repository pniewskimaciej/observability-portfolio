# Use Case 02 – Location-Based Marketing Feed

## Business Objective

The customer wanted to use mobile network location information as an input to **location-based marketing campaigns**.

The objective was to identify when subscribers approached predefined locations and provide this information to a downstream marketing platform, which could then determine whether an appropriate campaign should be triggered.

---

## Solution

I designed a custom feed based on data collected from the **S1-MME and SGs interfaces**.

The feed provided subscriber location information and was delivered to the customer's external **Apache Kafka broker** for further processing.

The customer could then correlate subscriber location with predefined points of interest and use the resulting information as an input to its marketing platform.

---

## Example Business Flow

```text
Mobile Network Activity
          │
          ▼
     S1-MME / SGs
          │
          ▼
   NETSCOUT Probes
          │
          ▼
     Custom Data Feed
          │
          ▼
   External Kafka Broker
          │
          ▼
 Customer Marketing Platform
          │
          ▼
 Location / Campaign Rules
          │
          ▼
   Targeted Campaign
```

---

## Feed Content

The feed contained key subscriber and location information, including:

* Timestamp
* MSISDN
* Cell ID / Location

The records were continuously exported to the customer's Kafka environment for downstream processing.

---

## Example Business Scenario

For example, when a subscriber entered the coverage area associated with a predefined point of interest such as a coffee shop, the customer's marketing platform could use the location event as an input to a campaign rule and potentially send the subscriber a relevant promotion.

The NETSCOUT feed provided the **network-derived location event**; campaign logic and customer communication were handled by the downstream customer systems.

---

## My Contribution

I designed and implemented the custom feed according to the customer's business and technical requirements, including:

* Identifying the required S1-MME and SGs data
* Defining the feed structure
* Selecting the required subscriber and location attributes
* Designing the data delivery mechanism
* Integrating the feed with the customer's external Kafka broker
* Supporting feed validation and troubleshooting
* Translating the customer's marketing use case into a technically viable network-data solution

---

## Technical Architecture

**Data Sources**

`S1-MME` · `SGs`

**Network Data**

`MSISDN` · `Cell ID` · `Timestamp`

**Data Collection**

`NETSCOUT Probes`

**Integration**

`Apache Kafka`

**Downstream Use**

`Location-Based Marketing` · `Campaign Automation`

---

## Skills Demonstrated

**Mobile Network Analytics · Location Intelligence · S1-MME · SGs · Custom Data Feeds · Kafka Integration · Telecom Data Engineering · Solution Design · Business-to-Technology Translation**

---

## Sample Data

A sample feed will be provided in:

`sample-feed.json`

The sample will be sanitized/synthetic and will not contain real subscriber information.

> **Important:** MSISDNs, Cell IDs, timestamps and other identifiers must be replaced or anonymized before publishing real examples publicly.
