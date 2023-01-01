# 📐 Reference Architecture

### Data flow design

The following is the reference data pipeline design to onboard large data sets.&#x20;

 

<figure><img src="../.gitbook/assets/large-data-onboarding-reference-architecture.drawio.png" alt=""><figcaption><p>Large data onboarding pipeline with storage gateway</p></figcaption></figure>

An outline of data onboarding steps are as follows:

1. Apply for Datacap
2. Fetch source dataset for data preparation.
3. Prepare source dataset into the **C**ontent-addressable **AR**chive ("CAR") format
4. Transfer CAR files to Storage Providers
5. Propose storage deals to SPs.
6. Each SP imports CAR files for storage deals and seals the data
7. Create an index for each dataset.
8. Test retrievals&#x20;

#### Storage Gateway

The "storage gateway" is a client-facing role responsible for data preparation, coordination with and deal-making with participating SPs. The organization running the storage gateway may recommend participating SPs based on individual client requirements. &#x20;

The _Storage Gateway_ role can be performed by any of:

* the _Lead Storage Provider,_\
  __The client onboarding experience is managed by a _Lead SP._ The lead SP serves as an advisor to the client, and performs data onboarding as a service for the Data Owner.
* the _Data Owner_,\
  When the data owner organization wants to take control of the onboarding process, and have the required technical skills and resources.
* an _independent_ _service provider_\
  __There may potentially be scope for an independent storage gateway market to develop, such as ISV, SaaS, and professional services offerings.&#x20;



###
