---
description: Define your data storage requirements and objectives
---

# 🔎 Select Datasets

### Dataset selection

When selecting the dataset to be stored into the Filecoin network, Data Owners may consider several of the following: data classification, use-cases, value of the data to the organization and for its users, costs of maintaining existing storage solution, and other reasons.

### Replication count and regional placements.

Determine how many replicas are required. Determine the desired regional placement of the replicas, from evenly-distributed across the planet, to a concentration of replicas in a few regions.



### Data Retention

Determine the duration the dataset needs to be retained for. The current maximum duration of Filecoin storage deals is 540 days. After this period, deals can be renewed by making new storage deals and re-sealing.

### Public or Private data

If the selected dataset is classified as public, it can be stored on the Filecoin network in clear and accessible the general public.

Private datasets will require the Data Owner to implement its own data privacy measures, for example, encryption. &#x20;

#### Encryption

Encryption of the dataset prior to storage is one way of enforcing data confidentiality over the Filecoin storage network. The Data Owner selects an encryption method, encrypts datasets prior to storage, and decrypts the datasets after retrieval. Data Owners are responsible for secret management and key management.

### Retrieval frequency

Consider the "Temperature" of data. Cold data storage and infrequent access are suitable for the Filecoin storage network. Consider what portion of the dataset will be requested for each retrieval, i.e. partial or full.&#x20;

The retrieval of hotter datasets that require frequent retrievals and with lower latency is outside the scope of this guide. Refer to [Filecoin Retrieval market](https://retrieval.market/) for projects implementing fast CDN retrievals.&#x20;

### Success objectives

Determine the success criteria, e.g. reducing storage costs, migrating from existing storage infrastructure, improving data availability and data durability, improving data decentralization, enabling new use-cases, Web 3 projects, etc. Plan for retrieval testing.
