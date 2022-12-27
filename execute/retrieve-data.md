# 📥 Data Retrieval

Singularity provides a user-friendly way to retrieve data using URI paths, similar to filesystem paths&#x20;

{% hint style="info" %}
This guide describes retrievals using the Singularity tool only. Filecoin retrievals are an evolving space, with projects working on fast CDN-type retrievals. See [https://retrieval.market/](https://retrieval.market/)&#x20;
{% endhint %}

### Prerequisites&#x20;

Singularity has completed the replication of a dataset.

SPs have sealed the dataset and deals are active on-chain.

IPFS daemon service is started.

### Create Index

Create the index for a named dataset:

```bash
singularity index create $DATASET_NAME_OR_ID
```

If your dataset contains a larger numbers of files that exceed default index soft-limits, you should increase the default parameters.

```
singularity index create --max-links $INDEX_MAX_LINKS \
  --max-nodes $INDEX_MAX_NODES $DATASET_NAME
```

This command writes the index to IPFS, and prints the IPFS path of the index in a DNS TXT record. &#x20;

```
Add or update a DNS TXT record for _dnslink.mydata.net
  _dnslink.mydata.net 34 IN TXT "dnslink=/ipfs/bafy..."
```

#### Publish the index with a user-friendly name (optional)

To make the IPFS path more user-friendly, a DNS TXT record for DNSLink can be published that contains the IPFS path, providing an easy logical name to reference the index.

E.g. If your organization owns the domain "mydata.net", and the dataset is named "mydatasetname" the DNSLink subdomain record can be:

```
  _dnslink.mydatasetname.mycorp.net 34 IN TXT "dnslink=/ipfs/bafy..."
```

Consult your DNS provider for specific instructions to update the TXT record.

**Alternate ways to reference IPFS paths (optional)**

If you do not have access to update the DNS provider of your organization, an alternative way is to use environment variables, aliases, or other indirection methods to dereference the IPFS path.

### List data&#x20;

Using DNSLink name:

```
singularity-retrieve ls -v singularity://ipns/mydata.net/
singularity-retrieve ls -v singularity://ipns/mydata.net/sub/path
```

Using the actual IPFS path.

```
singularity-retrieve ls -v "singularity://ipfs/bafy.../"
singularity-retrieve ls -v "singularity://ipfs/bafy.../sub/path"
```

### Retrieve data

Using DNSLink name:

```
singularity-retrieve cp -p $MINERID \
  singularity://ipns/mydata.net/sub/path $OUTPUT_PATH
```

Using the actual IPFS path.

```
singularity-retrieve cp -p $MINERID \
  "singularity://ipfs/bafy.../sub/path" <OUTPUT_PATH>
```

Based on [Indexing and Retrieval in the Singularity docs](https://github.com/tech-greedy/singularity/blob/main/getting-started.md#indexing-and-retrieval).

### Convenience helpers

Optionally, you can simplify user commands by defining aliases or helper scripts configured to the  index path in environment variables or aliases. E.g.

<pre><code><strong>fil-ls /sub/path
</strong>fil-cp /sub/path &#x3C;OUTPUT_PATH>
</code></pre>

Example implementations of fil-ls and fil-cp are at [https://github.com/frank-ang/filecoin-data-onboarding-tools/](https://github.com/frank-ang/filecoin-data-onboarding-tools/blob/master/lotus/fil-cp)





\




