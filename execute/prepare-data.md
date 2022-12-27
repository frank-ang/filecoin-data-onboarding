# 📦 Prepare Data

### 1. Preprocess dataset (optional)

The original dataset may be optionally pre-processed by the Data Owner, e.g. applying encryption to the source data. Encrypted data sets will require going through an E-Fil+ (Enterprise Filecoin Plus) application.

A trusted Data Preparer may provide advice and assistance to the Data Owner for encryption, e.g. recommend RSA/AES, GPG, or other encryption methods, and recommend secrets management approach. However, discussion of specific data encryption and key management options is outside the scope of this guide.

### 2. Transfer Source Data to Data Broker.

Source Data is transferred to the Data Preparer via a suitable method. The general choice is between either online data transfer or physical hard drive shipping.

When evaluating data transfer methods for large datasets, consider what is the optimal path:

* Network bandwidth
* Location of Data Preparer
* Offline data transfer, where suitable.\
  e.g. Seagate Lyve Mobile, Acromove, DIY shipment of encrypted hard drives, etc.

Budget for data transfer costs, e.g. online bandwidth, public cloud network egress fees, offline shipping.

### 2. Prepare Data

The Data Broker packages the Source Data into the [CAR format](https://ipld.io/specs/transport/car/), **C**ontent **A**ddressable a**R**chive.&#x20;

To use the Singularity tool to prepare a large dataset into CAR files:

```
singularity prep create MyDataset ~/dataset/folder ~/outDir 
```

This operation takes the Source Data, splits large files, bin-packs small files, packages the output into a set of CAR files of 32GB maximum size each, and registers the dataset metadata into the Singularity database.

Monitor the progress of data preparation:

```
singularity prep list
singularity prep status MyData
```

At the completion of data preparation, a set of CAR files become available in the output directory.

Further details in the [Singularity quick start guide](https://github.com/tech-greedy/singularity/blob/main/getting-started.md). &#x20;

### CAR padding and datacap (TODO)

Affects dataset sizing for datacap.





