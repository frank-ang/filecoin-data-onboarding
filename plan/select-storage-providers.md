# 🏢 Select Storage Providers

Select SPs that meet your requirements, endpoint presence in regions that match your regional replication requirements. For improved data availability and redundancy, plan for multiple replicas.

SPs can be selected from multiple sources:

* Starboard Ventures SPRD (Storage Provider Reputation Dashboard) [https://sprd.starboard.ventures/](https://sprd.starboard.ventures/)
* Filgram [https://filmine.io/filgram?type=active](https://filmine.io/filgram?type=active)
* Filecoin Plus Registry of miners [https://plus.fil.org/miners](https://plus.fil.org/miners)
* Ask for suggestions on Filecoin Slack. [https://filecoin.io/slack/](https://filecoin.io/slack/)

Data owners that prefer to delegate data onboarding tasks, should appoint a Lead SP as the Data Broker to execute data onboarding tasks, and to serve as the single point of coordination with participating SPs. In the case where a data owner already has a business relationship with an SP, this SP can serve as the Lead SP.

When evaluating participating SPs, consider SP reputation, location, operational reliability, storage retrievability, network bandwidth. Consider whether each SPs will store a full-replica or have replicas sharded across a larger number of SPs.

When planning a data distribution plan across all participating SPs, please align to the guidelines of Fil+:&#x20;

* Storage provider should not exceed 25% of total datacap.
* Storage provider should not be storing duplicate data for more than 20%.
* Storage provider should have published its public IP address.
* Storage providers should be located in different regions.
* No more than 25% of unique data are stored with less than 4 providers.
