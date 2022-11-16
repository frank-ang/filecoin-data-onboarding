# 📦 Prepare Data

### 1. Preprocess dataset (optional)

The original dataset may be optionally pre-processed by the Data Owner, e.g. adding encryption, to form the Source Data, ready for data preparation.&#x20;

### 2. Transfer Data to Data Preparer.

The Source Data is transferred to the Data Preparer via an agreed upon method. There are no restrictions on specific data transfer protocol or method. For example SCP, HTTPS, or physical hard drive shipping.

When evaluating possible routes for transferring a large dataset, consider:

* any optimal connectivity from Source Data to Data Preparer.\
  e.g. VPN, SD-WAN, AWS Transit Gateway, network peering, etc.
* any optimal placement of Data Preparer close to the Source Data. \
  e.g. co-location, if feasible.&#x20;
* any hybrid cloud connectivity from public cloud to on-premises, if applicable, \
  e.g. MPLS, AWS Direct Connect, etc.
* any offline data transfer options, where available.\
  e.g. Seagate Lyve Mobile, Acromove, DIY shipment of encrypted drives, etc.

The approach of one-time data transfer to a trusted Data Preparer can reduce data transfer costs for the Data Owner. The single Data Preparer executes data prep one single time in a consistent way.

Alternately, while Data Owners can transfer Source Data to each SP individually, please be mindful that the Data Owner may incur increased data transfer costs, e.g. public cloud network egress fees.&#x20;

### 2. Prepare Data

The Data Preparer is responsible for packaging the Source Data into the [CAR format](https://ipld.io/specs/transport/car/), i.e. Content Addressable aRchives.&#x20;

The Singularity tool prepares a large dataset into CAR files. E.g.

```
singularity prep create MyDataset ~/dataset/folder ~/outDir 
```

This operation takes the Source Data, splits large files, bin-packs small files, packages the output into a set of CAR files of 32GB maximum size each, and registers the dataset metadata into a local MongoDB database.

Further details in the [Singularity quick start guide](https://github.com/tech-greedy/singularity/blob/main/getting-started.md). &#x20;

###





