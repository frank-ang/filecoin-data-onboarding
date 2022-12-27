# 📐 Reference Architecture

### Data flow design

The following is the prescribed data pipeline design to onboard large data sets.&#x20;

<figure><img src="../.gitbook/assets/large-data-onboarding-reference-architecture.drawio.png" alt=""><figcaption><p>Data Broker Reference Architecture</p></figcaption></figure>

####

An outline of steps are as follows:

1. Apply for Datacap
2. Transfer source data for data preparation.
3. Prepare source data into the **C**ontent-addressable **AR**chive ("CAR") format
4. Storage Providers receives prepared CAR files from the Data Broker
5. Data Broker proposes storage deals to SPs.





#### Data Broker

The "Data Broker" role is responsible for data preparation, coordination with participating SPs, and to make storage deals with SPs. The Data Broker can recommend participating SPs that meet the data owner's requirements. The Data Broker functions as a trusted agent of the data owner.&#x20;

The Data Broker role can be performed by either of:

* the _Lead Storage Provider,_\
  __The onboarding experience is managed by an experienced and skilled Lead SP. The Lead SP becomes a trusted delegate of the Data Owner.
* the _Data Owner_,\
  When the data owner organization wants to take control of the onboarding process, and have the required technical skills and resources.
* an _independent_ _service provider_\
  __The Data Broker can potentially become a services business for vendors and systems integrators.



### 2. Data Transfer to Data Preparer.

The original dataset may be optionally pre-processed by the Data Owner, e.g. encryption, to form the Source Data. The Source Data can then be transferred to the Data Preparer using any online protocol or offline transport.

1-time online data transfer to a Data Preparer can reduce data transfer costs for the Data Owner, particularly if public cloud data egress fees apply. Other things to evaluate:

* hybrid cloud connectivity from public cloud to on-premises, if applicable.
* optimal connectivity from Source Data to Data Preparer, e.g. co-location, if feasible.&#x20;
* offline data transfer options, where available.

The Data Preparer is responsible for packaging the source data into the Filecoin CAR format, and staging the CAR files for distribution to the other participating SPs who will store replicas. The Data Preparer hosts the CAR files that participating SPs will fetch upon receipt of the online data transfer deal. Alternatively the SP will fetch&#x20;

### 3. Data Preparation

###

### 4. Distribute data to SPs

Determine the usable network bandwidth to a specific miner endpoint. Evaluate data transfer optimization such as aria2, HTTP protocol compression, etc. Calculate the estimate online data transfer time for the full dataset.

### 5. Propose Storage Deals

###
