---
title: "Comparison of S3 Deployment Modes: 3-AZ, 1-AZ, and Local Zones Overview"  
excerpt: "Explore OVHcloud's S3 Object Storage deployment modes"  
updated: "2024-10-24"  
---

## Objective

OVHcloud offers several deployment modes for its S3 Object Storage service, each tailored to specific needs regarding resilience, availability, performance, and latency. This document provides a detailed explanation of the characteristics of each deployment mode, followed by a comprehensive comparison to help users choose the best option for their requirements.

## Requirements

- Understanding the use cases for the different S3 deployment modes: 1-AZ, 3-AZ, and Local Zones.
- Familiarity with OVHcloud's S3 Object Storage service.

## Deployment modes

> **Note:**  
> The following information pertains to the different deployment modes available in OVHcloud’s S3 Object Storage service. Select the mode that best suits your needs based on resilience, availability, and performance. You can identify which deployment mode is available for a given region on the [Object Storage - Endpoints and geoavailability document.](https://help.ovhcloud.com/csm/en-gb-public-cloud-storage-s3-location?id=kb_article_view&sysparm_article=KB0047382)

### 1. Introduction to Deployment Modes

OVHcloud provides flexible S3 Object Storage deployment modes to meet different needs in terms of resilience, availability, and performance. Each mode is optimized for specific use cases and offers varying levels of redundancy and fault tolerance. This document explores these modes in detail and presents a comparison to facilitate informed decision-making.

### 2. 1-AZ Region

#### Infrastructure and Redundancy

A 1-AZ Region consists of a **single availability zone covering multiple data centers within the same region**, utilizing a 2N+1 redundancy design. This setup offers resilience against server rack and drive failures but may be vulnerable to a complete data center outage. Note that in a 1-AZ region, the Object Storage service is located in a specific data center, and if an outage occurs in the specific data center hosting the S3 service, access to data could be impacted, even if other data centers in the zone remain operational.

#### Characteristics

- **Erasure Coding:** Provides data redundancy across servers, ensuring continuity in the event of hardware failures by splitting data across multiple disks and servers within the availability zone.
- **Cost-Effectiveness:** A more affordable option, making it ideal for general-purpose applications and backups where cost is a primary concern.

#### Limitations:

- **Outage Risk:** In the event of a data center outage, data may become unavailable or potentially lost if the specific data center hosting the S3 service is impacted. However, protection against server rack and drive failures is maintained.

**Note:**  
To enhance resilience for critical applications in a 1-AZ Region, [asynchronous replication](https://help.ovhcloud.com/csm/en-gb-public-cloud-storage-s3-asynchronous-replication-buckets?id=kb_article_view&sysparm_article=KB0062422) can be employed, providing additional protection without compromising cost-effectiveness. This can help reinforce both application and data resiliency. An other option to mitigate this risk, we recommand using a [**3-AZ deployment mode**](#3-3-az-region).

#### Redundancy Specifications for 1-AZ:

| Parameter         | Description                                                               |
|-------------------|---------------------------------------------------------------------------|
| **Redundancy Type**   | 2N+1 across multiple data centers                                         |
| **Fault Tolerance**   | Server and disk-level fault tolerance; data center outage risk            |
| **Use Case Examples** | General-purpose applications, backups                                    |

### 3. 3-AZ Region

#### Infrastructure and Redundancy

3-AZ Regions consist of **three independent availability zones**, each isolated in terms of power, cooling, and network systems, providing true fault isolation. This architecture ensures **service availability** even if an entire availability zone experiences an outage.

#### Characteristics

- **High Availability:** Data remains available for both read and write operations, even in the event of a zone failure. This configuration is ideal for high-availability and fault-tolerant applications. 

#### Ideal Use Cases

3-AZ Regions are perfect for mission-critical and availability-sensitive applications where data governance requires continuous data availability, such as e-commerce or healthcare platforms, financial services, and live-streaming applications.

**Note:**  
While this setup offers robust protection, it may not be fully resilient to an unlikely regional outage. Additional protection, such as [multi-region asynchronous replication](https://help.ovhcloud.com/csm/en-gb-public-cloud-storage-s3-asynchronous-replication-buckets?id=kb_article_view&sysparm_article=KB0062422), can be considered to further enhance data availability and resilience.

#### Performance Specifications for 3-AZ:

| Parameter         | Description                                                               |
|-------------------|---------------------------------------------------------------------------|
| **Connectivity**      | Low latency between availability zones                                    |
| **High Availability** | Maintains access even with zone failures                                  |
| **Use Case Examples** | Mission-critical and availability-sensitive applications, streaming, e-commerce, healthcare |

### 4. Local Zones

#### Design and Flexibility

Local Zones are designed to bring OVHcloud services closer to end-users, minimizing latency and ensuring compliance with local data regulations. These zones are particularly useful for applications that require minimal response times.

#### Benefits for Compliance and Cost

- **Reduced Network Costs:** Local Zones help reduce costs by minimizing the distance that data must travel.
- **Localized Storage:** Supports regional data localization requirements, making it ideal for regulatory compliance.

#### Limitations

- **Single Zone Limitation:** Local Zones are limited to a single availability zone and do not provide cross-zone redundancy, which limits data recovery options in the event of a disaster.

#### Use Case Specifications for Local Zones:

| Advantage        | Description                                           |
|------------------|-------------------------------------------------------|
| **Performance**      | Ultra-low latency for maximum performance             |
| **Data Compliance**  | Supports data localization for regulatory requirements|
| **Use Case Examples**| Online gaming, video conferencing, regional applications |

### 5. Comprehensive Comparison Table

| Characteristics        | 1-AZ Region                         | 3-AZ Region                     | Local Zones                              |
|------------------------|-------------------------------------|---------------------------------|------------------------------------------|
| **Deployment Structure**    | Single availability zone            | Three independent availability zones | Localized for low latency                |
| **Redundancy**             | 2N+1 internal                       | Cross-zone redundancy            | No inter-zone redundancy                 |
| **Data Availability**      | Limited during data center outages, protected against server/disk failures | Maintained across availability zones | Limited to the local zone                |
| **Latency**               | Moderate                            | Low between availability zones   | Ultra-low for end-users                  |
| **Ideal Use Cases**        | General-purpose applications, backups | Mission-critical and availability-sensitive applications | Latency-sensitive, regional applications |
| **Cost**                   | Lower                               | Higher due to increased redundancy | Dependent on the specific local zone and required latency performance |

## Go Further

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](https://www.ovhcloud.com/en-ie/professional-services/) to get a quote and ask our Professional Services experts for assisting you on your specific use case.

Join our community of users on <https://community.ovh.com/en/>.
