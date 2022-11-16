# 📥 Retrieve Data



{% hint style="info" %}
This guide describes retrievals using the Singularity tool. Please note the projects within the Filecoin Retrievals Market will enhance retrievals, and is a rapidly-evolving space. Find out more at [https://retrieval.market/](https://retrieval.market/)&#x20;
{% endhint %}

TODO

See [Indexing and Retrieval in the Singularity docs](https://github.com/tech-greedy/singularity/blob/main/getting-started.md#indexing-and-retrieval).

1. Install [IPFS](https://docs.ipfs.tech/install/) and start the daemon service
2. Create index.\
   `singularity index create MyDataset`
3. Publish the IPFS path with DNSLink\
   `Add or update the TXT record for _dnslink.mydata.net`\
   `_dnslink.mydata.net 34 IN TXT "dnslink=/ipfs/bafy..."`
4.  Browse and Retrieve the dataset (copy pasted from singularity docs)

    ```
    # ls command tells what file or folder is inside the sub path of the dataset
    singularity-retrieve ls -v singualrity://ipns/mydata.net/sub/path
    # show command tells the CID of the file or folder and how to assemble them back 
    singularity-retrieve show singualrity://ipns/mydata.net/sub/path
    # cp command retrieves the data from a specific storage provider to a local path and reassemble them if needed
    singularity-retrieve cp -p f01111 singualrity://ipns/mydata.net/sub/path ./local/path
    ```

    ###

    \


    \




