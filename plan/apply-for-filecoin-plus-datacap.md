# 🎟 Apply for Filecoin Plus DataCap

### What is DataCap?

DataCap is a cryptoeconomic incentive to Storage Providers for storing verified datasets. Clients apply for DataCap, which is reviewed by a community of Fil+ notaries. Upon approval, DataCap is allocated to the applicant's FIL wallet. DataCap is spent by the client in storage deals with storage providers. In a way, DataCap can be thought of as similar to storage credits.&#x20;

Datacap is part of the Fil+ (Filecoin Plus) programme. More info about Fil+ Plus:

* [https://docs.filecoin.io/store/filecoin-plus/](https://docs.filecoin.io/store/filecoin-plus/)
* [https://github.com/filecoin-project/filecoin-plus-client-onboarding](https://github.com/filecoin-project/filecoin-plus-client-onboarding)
* [https://github.com/filecoin-project/filecoin-plus-large-datasets](https://github.com/filecoin-project/filecoin-plus-large-datasets)

### Prepare a Filecoin wallet

The wallet address will be where approved Fil+ datacap will be allocated to.&#x20;

To create a Filecoin wallet on a lotus node, see [wallet instructions on lotus docs](https://lotus.filecoin.io/tutorials/lotus/store-and-retrieve/set-up/#get-a-fil-address).

To create a Filecoin wallet on Boost client, see [boost init command on boost docs](https://boost.filecoin.io/getting-started/boost-client).

Please securely backup the wallet keys, using `lotus wallet export` or `boost wallet export` commands &#x20;

Question> How to use same datacap wallet across lotus and boost?

### Apply for **Large Dataset Datacap Application**&#x20;

Create a Large Dataset Datacap Application as a Github issue at:\
[https://github.com/filecoin-project/filecoin-plus-large-datasets/issues](https://github.com/filecoin-project/filecoin-plus-large-datasets/issues),  \
click "New Issue" -> Large Dataset Notary application -> "Get Started".

Alternately, use [https://filplus.storage/apply](https://filplus.storage/apply) &#x20;

{% hint style="info" %}
Where possible, apply for datacap using a Github account with some history of commits or repository activity, to better align with Github terms of service.
{% endhint %}

The datacap application process can take several days of governance review. Q\&A about the application can extend the duration, so it is recommended to provide clear and complete information, clearly describe the use-case, be transparent. When in doubt, over-communicate details. Click "subscribe" to receive questions and comments on the Datacap application, so that you can respond promptly to questions from the Filecoin governance community.

Each datacap application has a maximum datacap limit of 5 PiB. For datasets that exceed 5 PiB, one approach is to submit a multi-part series of LDNs.&#x20;

{% hint style="info" %}
Plan for an additional amount of datacap as buffer, as the storage deals are sized based on the total padded Content Addressable aRchive (CAR) files. The size of each CAR file must be a power of two, so when data is packed into CAR files, padding is often added. There is typically not 100% efficiency in data packing.
{% endhint %}





{% embed url="https://docs.filecoin.io/get-started/store-and-retrieve/set-up/#filecoin-plus" %}
