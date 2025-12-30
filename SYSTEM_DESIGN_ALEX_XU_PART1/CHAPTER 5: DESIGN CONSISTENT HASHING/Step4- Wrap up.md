##### Wrap up

* we had in-depth disucussion about consistent hashing, including why it is needed and how it works. 
* Benefits of consistent hashing include:
    * Minimized keys are redistributed when servers are added or removed.
    * It is easy to scale horizontally, because data are evenly distributed.
    * Mitigate hotspot key problem. Excessive access to specific shard could increase the server overload. Say, access to celebrities data can be handled by consistent hashing by distributing the data evenly.
* Consistent hashing is widely used in real-world systems, including some notable ones:
    * Partitioning component of Amazon's Dynamo database.
    * Data Partitioning across the cluster in Apache Cassandra.
    * Discord chat application.
    * Akamai content delivery network.
    * Maglev network load balancer.
  