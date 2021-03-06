# Distributed Systems

> A collection of independent computers that appear to its users as one computer. **- Andrew Tannenbaum**

### Three Characteristics

- The computers operate concurrently
- The computers fail idependently
- The computers do not share a global clock

### Tools:

- **Storage:** Relation/Mongo, Cassandra, HDFS 
- **Computation:** Hadoop, Spark, Storm
- **Synchronization:** NTP, vector clocks
- **Consensus:** Paxos, Zookeeper
- **Messaging:** Kafka

### Technique

- [Partitioning](https://en.wikipedia.org/wiki/Partition_(database)#Partitioning_methods)
- [Replication](https://en.wikipedia.org/wiki/Replication_(computing))
- [Sharding](https://en.wikipedia.org/wiki/Shard_(database_architecture))
- [Consistent Hashing](https://www.toptal.com/big-data/consistent-hashing)
- **Distributed Transactions**
- [The Raft Consensus Algorithm](https://raft.github.io/)

# [Databases](https://db-engines.com/en/system/Amazon+Aurora%3BAmazon+DynamoDB%3BGoogle+Cloud+Spanner%3BMicrosoft+Azure+Cosmos+DB%3BMicrosoft+SQL+Server)
- [Build modern apps with big data at a global scale](https://www.arbelatech.com/insights/white-papers/build-modern-apps-with-big-data-at-a-global-scale) - pdf
- [Amazon Aurora](docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html)
- [Amazon DynamoDB](docs.aws.amazon.com/dynamodb)
- [Google Cloud Spanner](	cloud.google.com/spanner/docs)

### Quora/Stackoverflow Q&A
- Stackoverflow
  - [Difference between Sharding and Replication](https://stackoverflow.com/a/11571916/5200896)
- Quora
  - [Why is MongoDB losing popularity?](https://www.quora.com/Why-is-MongoDB-losing-popularity)


# [Types of databases](https://medium.com/swlh/4-types-of-nosql-databases-d88ad21f7d3b)

- SQL Databases
  - Relational (OLTP)
  - Analytical (OLAP)
- NoSQL Databases
  - Document databases
  - Key-value stores
  - Column-oriented databases
  - Graph databases


# System Properties Comparison

- [Amazon Aurora vs. Amazon DynamoDB vs. Google Cloud Spanner vs. Microsoft Azure Cosmos DB vs. Microsoft SQL Server](https://db-engines.com/en/system/Amazon+Aurora%3BAmazon+DynamoDB%3BGoogle+Cloud+Spanner%3BMicrosoft+Azure+Cosmos+DB%3BMicrosoft+SQL+Server)
- [Amazon DynamoDB vs. Cassandra vs. CouchDB vs. Riak KV](https://db-engines.com/en/system/Amazon+DynamoDB%3BCassandra%3BCouchDB%3BRiak+KV)
- [Aerospike vs. Couchbase vs. Redis](https://db-engines.com/en/system/Aerospike%3BCouchbase%3BRedis)

# CAP Theorem

### [ACID](https://en.wikipedia.org/wiki/ACID)
### [BASE]()

### [High Availability](https://en.wikipedia.org/wiki/High_availability)

- [What is High Availability?](https://www.digitalocean.com/community/tutorials/what-is-high-availability) - digitalocean.com
- [Floating IPs: Start Architecting Your Applications for High Availability](https://blog.digitalocean.com/floating-ips-start-architecting-your-applications-for-high-availability/) - digitalocean.com

### Messaging
- [Message Delivery Reliability](https://getakka.net/articles/concepts/message-delivery-reliability.html) - getakka.net
- [Nobody Needs Reliable Messaging](https://www.infoq.com/articles/no-reliable-messaging/) - infoq.com
- [Erlang documentation](http://erlang.org/faq/academic.html) - erlang.org
- [How to Guarantee Delivery of Messages in Akka.NET](https://petabridge.com/blog/akkadotnet-at-least-once-message-delivery/) - petabridge.com
### Wikis
- [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem) - wikipedia.com
- [PACELC theorem](https://en.wikipedia.org/wiki/PACELC_theorem) - wikipedia.com
- [CRDT - Conflict-free replicated data type](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type)

### Daniel Abadi posts

- [Problems with CAP, and Yahoo’s little known NoSQL system](http://dbmsmusings.blogspot.com/2010/04/problems-with-cap-and-yahoos-little.html)
- [Replication and the latency-consistency tradeoff](http://dbmsmusings.blogspot.com/2011/12/replication-and-latency-consistency.html)
- [Distributed consistency at scale: Spanner vs. Calvin](http://dbmsmusings.blogspot.com/2017/04/distributed-consistency-at-scale.html)
- [NewSQL database systems are failing to guarantee consistency, and I blame Spanner](http://dbmsmusings.blogspot.com/2018/09/newsql-database-systems-are-failing-to.html)
- [Hazelcast and the Mythical PA/EC System](http://dbmsmusings.blogspot.com/2017/10/hazelcast-and-mythical-paec-system.html)

### Papers

- [The End of an Architectural Era(It’s Time for a Complete Rewrite)](http://nms.csail.mit.edu/~stavros/pubs/hstore.pdf)
- [Spanner, TrueTime &
The CAP Theorem](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45855.pdf) - by Eric Brewer
- [Dynamo: Amazon’s Highly Available Key-value Store](http://s3.amazonaws.com/AllThingsDistributed/sosp/amazon-dynamo-sosp2007.pdf)
- [Consistency Tradeoffs in Modern Distributed Database System Design](http://www.cs.umd.edu/~abadi/papers/abadi-pacelc.pdf) - by Daniel Abadi
- [CAP Twelve Years Later: How the “Rules” Have Changed](https://sites.cs.ucsb.edu/~rich/class/cs293b-cloud/papers/brewer-cap.pdf) - by Eric Brewer
- [Harvest, Yield, and Scalable Tolerant Systems](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.24.3690&rep=rep1&type=pdf) - by Eric Brewer
- [Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.67.6951&rep=rep1&type=pdf)

### Slides
- [Towards Robust Towards Robust Distributed Systems Distributed Systems](https://people.eecs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf)

### Documentations
- [What is the CAP Theorem?](https://apple.github.io/foundationdb/cap-theorem.html) - FoundationDB

# Glossary
### [Amazon's Dynamo](https://www.allthingsdistributed.com/2007/10/amazons_dynamo.html)
- Partitioning
  - Consistent Hashing
- Handling temporary failures
  - Sloppy Quorum 
  - Hinted handoff
- Conflicts
  - LWW - Last Write Win
  - Vector Clocks
  - [CRDT - Conflict-free replicated data type](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type)
    - [Delta CRDT](https://arxiv.org/pdf/1603.01529.pdf)
    - [A Conflict-Free Replicated JSON Datatype](https://arxiv.org/pdf/1608.03960.pdf)
- Membership and failure detection
  - Gossip-based membership protocol and failure detection.

- Consensus Algorithms
  - [Paxos](https://en.wikipedia.org/wiki/Paxos_(computer_science)) - wikipedia.org
  - [Raft](https://raft.github.io/) - raft.github.io
  - [Zab](https://cwiki.apache.org/confluence/display/ZOOKEEPER/Zab+vs.+Paxos)
- Service Discovery Systems
  - [Zookeeper](https://zookeeper.apache.org/doc/r3.6.2/zookeeperInternals.html)
  - [Consul](https://www.consul.io/docs/intro)
  
- Multi-Master Replication
- Replication Factor
- Bidirectonal Replicaiton
...

# Stream Processing
- Spark
- Flink
- Samza
- Hadoop
- [Comparing Apache Spark, Storm, Flink and Samza stream processing engines - Part 1](https://blog.scottlogic.com/2018/07/06/comparing-streaming-frameworks-pt1.html)
