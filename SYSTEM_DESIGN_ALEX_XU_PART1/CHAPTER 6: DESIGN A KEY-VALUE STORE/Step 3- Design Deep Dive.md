**System components:**

Core components and techniques used to build a Distributed Key-Value Store:

**1. Data partition:** 

For large applications, It is infeasible to fit the complete data set in a single server. The simplest way to accomplish this is to split data into smaller portions and store them in multiple servers. There are two challenges while partitioning data:

* Distribute data across multiple servers evenly.
* Minimize data movement when nodes are added or removed.

**Consistent Hashing at a high level :**

* First servers are placed on a hash ring,  eight servers, represented by s0, s1,....s7 are placed in the hash ring.
* Next, a key is hashed onto the same ring, and is allocated first server encountered in clockwise direction.

![alt text](images/ConsistentHashingatHighlevel.png)

* For instance, key0 is stored in s1 using this logic.
  
Data partition has following advantages when consistent hashing is used:

* **Automatic scaling:** servers could be added and removed automatically depending on the load.
* **Heterogeneity:** The number of virtual nodes for a server depends upon the capacity of the server. For example, servers with high capacity are assigned with more virtual nodes.

**Data replication:**
To achieve high availability and reliability, data must be replicated asynchronously over N servers, where N is a configurable parameter.  These N servers are chosen using following logic: after a key is mapped to a position on the hash ring, walk clockwise from that position and choose first N srevers on the ring to store the data copies.

![alt text](images/Datareplication.png)

In the above figure, key0 is replicated at s1,s2 and s3.

With virtual nodes, the first N nodes on the ring may be owned by fewer than N physical servers. To avoid this issue, we only choose unique servers while performing the clockwise walk logic.

Nodes in the same data center often fail at the same time due to power outrages, network issues, natural disasters etc., For better reliability, replicas are placed in distinct data centers and data centers are connected through high speed networks.

**Consistency:**
Since data is replicated at multiple nodes, it must be synchronized across replicas. Quorum consensus can guanrantee consistency for both read and write operations, 

**N** = The number of replicas
**W** = A write quorum size of W. The write operation from W replicas sends the acknowledgment once the write operation is successful.
**R** = A read quorum of size R. For read operation to be considered as successful, read operation must wait for responses from at least R replicas.


![alt text](images/Consistency.png)



