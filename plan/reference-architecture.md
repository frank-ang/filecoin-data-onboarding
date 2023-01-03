# 📐 Reference Architecture

### Data flow design

The following is the reference data pipeline architecture to onboard large data sets.&#x20;

 

<figure><img src="../.gitbook/assets/large-data-onboarding-reference-architecture.drawio.png" alt=""><figcaption><p>Large data onboarding pipeline with storage gateway</p></figcaption></figure>

The outline of data onboarding steps (numbered circles) as follows:

1. Data Owner applies for Datacap, to be allocated to the client wallet.
2. Gateway fetches source dataset.
3. Gateway prepares source dataset into **C**ontent-addressable **AR**chive ("CAR") formatted files.
4. SPs downloads CAR files
5. Gateway proposes storage deals to SPs.
6. SPs imports the CAR files corresponding to Storage Deals. Seals the data into sectors.
7. Create an index for each dataset.
8. Browse and Retrieve files from the dataset.&#x20;

#### Storage Gateway

The "_Storage Gateway_" is a client-facing role responsible for data preparation, coordination with and deal-making with participating SPs. The organization running the storage gateway may recommend participating SPs based on individual client requirements. &#x20;

The _Storage Gateway_ function can be performed by any of:

* the _Data Owner_,\
  When the data owner organization wants to take control of the onboarding process, and have the required technical skills and resources.
* the _Lead Storage Provider,_\
  __The client onboarding experience is managed by a _Lead SP._ The lead SP serves as an advisor to the client, and performs data onboarding as a service for the Data Owner.
* an _independent_ _service provider_\
  __There may potentially be scope for a storage gateway market to develop, possibly provided by ISV, SaaS, and other service providers.&#x20;



###
