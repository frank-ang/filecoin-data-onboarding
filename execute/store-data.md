# ▶ Store Data

### 3. Data Preparer transfers data to SPs

Prepared CAR files can be distributed to SPs Online or Offline.&#x20;

This this guide describes the **Off**line data transfer mode.

#### **3.1. Online data transfer**&#x20;

Upon receipt of each Storage Deal Proposal, the associated CAR file data is transferred to the SP**.** Data transfer protocol can be HTTPS for Boost deals, or GraphSync for legacy deals. Boost also permits the files to be staged on a web server by the Data Preparer, such that SPs can pull the CAR file URL referenced in each deal. One should be mindful of bandwidth limits, congestion, and SP sealing throughput, which may require throttling of batches.

Essentially, the deal proposal and data transfer of the associated deal data occurs in one operation. This is suitable for cases where online networking is highly reliable for the dataset size.

#### 3.2. Offline (i.e. "out-of-band") data transfer

More typically for large datasets,&#x20;

1. The SP pre-fetches the CAR files from the Data Preparer "out-of-band", _prior_ to receiving Storage Deal proposals. &#x20;
2. The SP then receives Storage Deal proposals without corresponding CAR data transfer. These deals remain in an incomplete state until the corresponding data is imported.&#x20;
3. The SP then imports the matching CAR file for each Storage Deal, matched by `dataCid`. \
   E.g. using the Singularity import script `auto-import-boost.sh` or `auto-import.sh` , depending on the version of Lotus markets. Sealing can then proceed.

There are several benefits with the out-of-band/offline approach. By receiving CAR files prior to deal making, an SP:

* Reliability. Avoids online data transfer networking failures during deal making.&#x20;
* Control. SP has finer control over their sealing pipeline throughput.&#x20;
* Optimizations. Out-of-band network optimizations can be utilized such as aria2, HTTP gzip compression.
* Flexibility. No restriction on out-of-band data transfer methods, e.g. HTTPS, SCP, Rsync, S3, enterprise managed file transfer products, physical hard drive shipping.&#x20;

The Data Preparer should evaluate, test, and select an optimal data transfer method for each SP endpoint.&#x20;

Further reading in the Lotus docs about [deals with offline data transfer](https://lotus.filecoin.io/tutorials/lotus/large-files/#deals-with-offline-data-transfer).

### 4. Data Preparer proposes storage deals to SP(s)

The Data Preparer proposes Storage deals to SPs. E.g. using [Singularity](https://github.com/tech-greedy/singularity/blob/main/getting-started.md):

```
# singularity repl start --max-deals <n> <dataset_id> <storage_providers> <client_address>
singularity repl start --max-deals 10 MyDataset f01111 f1...
```

By default, Singularity sends the storage deal proposals as "offline" mode. This means that while the deal proposal itself is transmitted to the SP online, the actual dataset content is expected to be sent out-of-band, so the SP does not automatically fetch the dataset content upon receipt of the deal proposal.&#x20;



### 5. SP imports data for deals

The SP then imports the matching CAR file for each Storage Deal, matched by `dataCid`. &#x20;

(TODO: or is it the Piece Commitment CID / CommP?)\
E.g. using the Singularity import script `auto-import-boost.sh` or `auto-import.sh` , depending on the version of Lotus markets. Sealing can then proceed.



```
// Some code
TODO: code sample and input file format for script.

```

``

