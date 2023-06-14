Apache Kafka is an open-source distributed event streaming platform used by thousands of companies for high-performance data pipelines, streaming analytics, data integration, and mission-critical applications.

## CORE CAPABILITIES
* High Throughput: Deliver messages at network limited throughput using a cluster of machines with latencies as low as 2ms.
* Scalable
* Permanent storage: Store streams of data safely in a distributed, durable, fault-tolerant cluster.
* High availability

## Use Cases
* Messaging
* Website tracking activity
* Capturing Metrics
* Log Aggregation
* Stream processing
* Event sourcing
* Commit log


## Kafka Event Streaming
Kafka combines three key capabilities
* To publish (write) and subscribe to (read) streams of events, including continuous import/export of your data from other systems.
* To store streams of events durably and reliably for as long as you want.
* To process streams of events as they occur or retrospectively.

## How does Kafka works?

* Kafka is a distributed system consisting of servers and clients
* Server and client communicate via a high-performance TCP network protocol.


## Concepts:
* Event (Record/Message/Event): An event records the fact that "something happened" in the world or in your business
* Producer: Produce events
* Consumer: Subscribe and consumes the events
* Topics

## Topics
* Events are organized and durably stored in topics. 
* To be simplified A topic is similar to a folder in a filesystem, and the events are the files in that folder.
* Ex: payment, order ..etc
* A topic can have zero, one, or many producers that write events to it, as well as zero, one, or many consumers that subscribe to these events. 
* Kafka allows events to be read repeatedly and does not delete them after consumption. You can configure how long events are retained, and Kafka's performance remains constant regardless of data size, making long-term storage feasible.
* Topics are partitioned, meaning a topic is spread over a number of "buckets" located on different Kafka brokers. 
* Events with the same event key (e.g., a customer or vehicle ID) are written to the same partition,  
* Kafka guarantees that any consumer of a given topic-partition will always read that partition's events in exactly the same order as they were written.

## Kafka Connect
*  Kafka Connect allows you to continuously ingest data from external systems into Kafka, and vice versa. 
*  Ex: You probably have lots of data in existing systems like relational databases or traditional messaging systems, along with many applications that already use these systems
*  