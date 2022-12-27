---
description: Define your data storage requirements and objectives
---

# 🔎 Select Datasets

### Dataset selection

When selecting the dataset to be stored into the Filecoin network, Data Owners should consider: data classification, use-cases, value of the data, costs and issues with an existing storage solution.

The total sizing of a "large dataset" multiplied to include all replicas, is typically defined as between 500TiB to 5 PiB size, including all replicas.

#### Sizing and Regional placement

Determine how many replicas are needed, and. It is recommended to plan for multiple replicas, to increase data availability and durability. Consider distributing replicas across geographic regions for closer access from distributed users. Consider any data residency regulations that may limit replicas to within a country.

#### Data Retention

Determine the duration the dataset needs to be retained for. The current maximum duration of Filecoin storage deals is 540 days. After this period, deals can be renewed by making new storage deals and re-sealing.

### Public or Private data

If the selected dataset is classified as public, it can be stored on the Filecoin network in clear and accessible the general public.

Private datasets will require the Data Owner to implement encryption for data privacy. &#x20;

#### Encryption

Encryption of the dataset by the Data Owner prior to storage is one way of enforcing data confidentiality over the Filecoin storage network. The Data Owner selects an encryption method, encrypts datasets prior to packaging and storage, and decrypts the datasets after retrieval. Data Owners are responsible for secret management and key management.

An experienced Data Preparer can provide advice to the Data Owner on encryption methods and secrets management.

TODO: Insert DSS actual scripts.

### Retrieval frequency

Consider the "Temperature" of data. Cold data storage and infrequent access of archived data is currently a suitable use-case for the Filecoin storage network. Consider what portion of the dataset will be requested for each retrieval, i.e. partial or full. Consider whether the data should be retrieved online, offline data transfer arrangement can be negotiated with the Lead SP.&#x20;

The retrieval of hotter datasets that require frequent retrievals and with lower latency is an evolving space, but outside the scope of this guide. Refer to [Filecoin Retrieval market](https://retrieval.market/) for projects working on fast CDN retrievals on Filecoin.&#x20;

### Success objectives

Determine the success criteria, e.g. reducing storage costs, improvement from existing storage infrastructure, improving data availability and data durability, improving data decentralization, enabling Web3 use-cases, etc.&#x20;

Plan for retrieval testing.
