# ⚒ Setup Data Broker environment

### Data Broker server

For Lead SPs performing the Data Broker role, a typical placement is at the Lead SP's datacenter.&#x20;

Note that On-premises hosting may be more cost-effective than hosting on public cloud, when considering potentially high cloud data egress fees.

#### Storage

Data preparation is IO-bound, so fast local or network storage is recommended. Storage sizing should provision sufficient space for the dataset to be prepared and the output CAR files.

#### Network bandwidth

Data transfer flows from the Source Data to the Data Broker 1-time.

Prepared CAR files are hosted by the Data Broker for download by participating SPs.&#x20;

For network data transfer, estimate the bandwidth required and transfer duration to each SP. Receiving SPs should also have sufficient bandwidth. For SPs that will use physical hard drive shipping can reduce the bandwidth required.

**Software**

The Data Broker server should be installed with:

* [Singularity](https://singularity.storage/) - petabyte-scale data onboarding and retrieval client tool&#x20;
* [Lotus Lite node](https://lotus.filecoin.io/lotus/install/lotus-lite/) - a lite client for interacting with the Filecoin chain. Used for legacy deals.
* [Boost](https://boost.filecoin.io/) - the new lotus markets client used for newer v1.2 deals
* Web Server - hosting of CAR files for online data transfer to SPs. E.g. Nginx.
* [IPFS](https://docs.ipfs.tech/install/) daemon, stores the Singularity dataset index for retrievals.

It is recommended to use an Ubuntu Linux instance and build the Singularity, Lotus node, and Boost packages from source.

An example script to build and install the above stack is at \[**TODO** link to repo]

**Example project configuration and results.**

**TODO**: insert DSS actual sizing and results as guideline.





