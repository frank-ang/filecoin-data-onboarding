# ⚒ Setup Storage Gateway environment

## Architectural decisions

#### Data transfer plan and Gateway placement

Network data transfer is often a limiting factor when onboarding PiB-scale large data sets. Determine the optimal data replication approach for the following paths:

* Source dataset replicated from the data owner to the storage gateway,
* Prepared dataset replicated from the storage gateway to each participating SP.

Compare online network data transfer options and offline physical media transport options, consider feasibility, cost, transfer duration, etc. The data transfer plan may also affect the optimal placement the storage gateway. Compare cloud vs. on-premise hosting. Consider the physical locations of the source dataset and the destination SPs.

#### Storage selection and sizing

Gateway storage should be sized accordingly for the source dataset, and for hosting of the prepared CAP files. Data preparation is IO-bound, and the storage gateway will benefit from fast temporary local storage, such as iSCSI or NVMe storage interfaces.&#x20;

**Software stack**

The storage gateway server should be installed with:

* [Singularity](https://singularity.storage/) - petabyte-scale data onboarding and retrieval client tool&#x20;
* [Lotus Lite node](https://lotus.filecoin.io/lotus/install/lotus-lite/) - a lite client for interacting with the Filecoin chain. Used for legacy deals.
* [Boost](https://boost.filecoin.io/) - a new lotus markets client. Used for newer v1.2 deals
* Web Server - hosting of CAR files for online data transfer to SPs. E.g. Nginx.
* [IPFS](https://docs.ipfs.tech/install/) daemon, stores the Singularity dataset index for retrievals.

An Ubuntu Linux instance is recommended. Singularity, Lotus node, and Boost packages can be built and installed from source.

An example script to build and install the above stack is at \[**TODO** link to repo]

### **Example actual gateway configuration and project results**

**TODO**: insert DSS actual sizing and results as guideline.





