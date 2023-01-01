---
description: Define your data storage requirements and objectives
---

# 🔎 Select Datasets

### Dataset selection

When selecting the dataset to be stored into the Filecoin network, Data Owners should consider: data classification, use-cases, value of the data, costs and issues with an existing storage solution.

The total sizing of a "large dataset" multiplied to include all replicas, is typically defined as larger than 500TiB, including all replicas.

### Dataset Sizing&#x20;

Determine the size of the source dataset.&#x20;

Determine how many replicas are needed. Multiple replicas across multiple SPs will increase data availability, durability, and fault-tolerance. To calculate the total size, multiply the source dataset by the number of replicas.&#x20;

### Replica placement

Where possible, it is recommended to distribute replicas to multiple SPs across geographic regions. Consider any data residency regulations that may limit replicas to within a country.

### Data Retention

Determine the duration the dataset needs to be retained for. The current maximum duration of Filecoin storage deals is 540 days. After this period, deals can be renewed by making new storage deals and re-sealing.

### Public or Private data

If the selected dataset is classified as public, it can be stored on the Filecoin network in clear and accessible the general public.

Private datasets will require the Data Owner to implement encryption for data privacy. &#x20;

#### Encryption

Encryption of the dataset by the Data Owner prior to storage is one way of enforcing data confidentiality over the Filecoin storage network. The Data Owner selects an encryption method, encrypts datasets prior to packaging and storage, and decrypts the datasets after retrieval. Data Owners are responsible for secret management and key management.

An experienced Data Preparer provide advice to the Data Owner on encryption methods and secrets management.

TODO: Insert DSS actual scripts.

### Retrieval frequency

Consider the "Temperature" of data. Cold data storage and infrequent access of archived data are suitable use-cases for storage on the Filecoin network. Currently, retrieval service levels should be agreed upon with individual SPs.

Consider what portion of the dataset will be requested for each retrieval, i.e. partial or full. Consider whether the data should be retrieved online, offline data transfer arrangement can be negotiated with the Lead SP.

{% hint style="info" %}
Fast and lower-latency retrieval of hotter datasets is work-in-progress, and beyond the scope of this guide. Refer to [Filecoin Retrieval market](https://retrieval.market/) for more info.&#x20;
{% endhint %}

### Define project objectives&#x20;

Determine the project objectives, e.g. reducing storage costs, improvement from existing storage infrastructure, improving data availability and data durability, improving data decentralization, enabling Web3 use-cases, etc.&#x20;

Plan for retrieval testing.
