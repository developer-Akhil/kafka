# kafka


![image](https://github.com/user-attachments/assets/6396a0a5-85d8-4e9a-8787-602d11aeeb88)

# Topic
A topic is a unique name for kafka stream.

Each topic has a name that is unique across the entire Kafka cluster.

You can have as many topics as you want.

A topic is identified by its name.

Like a table in database (without all the constraints)

The sequence of message is called a data stream.

You cannot query topics, instead, use kafka Producers to send data and kafka Consumers to read the data.

![image](https://github.com/user-attachments/assets/b555b147-a683-4314-a4e9-07c4c5f0e451)

![image](https://github.com/user-attachments/assets/82bae9ea-b595-434d-967f-ac679092035a)

In Kafka, a partition is not a file or a physical storage unit, but rather a logical unit of organization for data within a topic. Each partition is a sequence of ordered, immutable records (messages) that belong to a specific topic. Partitions serve as the basic building blocks for data distribution, parallelism, and scalability in Kafka.

![image](https://github.com/user-attachments/assets/dddf0fb4-d62a-471c-8d35-19219f85532d)

![image](https://github.com/user-attachments/assets/0beb83ec-11ab-4e27-80ce-baea1ea3dd04)

A Kafka producer is responsible for publishing data to a Kafka topic. It is a client application that sends messages or records to a Kafka cluster, which is a collection of Kafka brokers that work together to manage the storage and replication of data.
Producers can be written in different programming languages and can be deployed on different servers. When a producer sends a message to a Kafka topic, it is stored in a partition within that topic. The message is then replicated across multiple brokers to ensure fault tolerance and high availability.
 
![image](https://github.com/user-attachments/assets/04da8cea-6605-4cb7-9770-004e77224d40)

![image](https://github.com/user-attachments/assets/f610a518-0266-4f0a-a44d-ce8f2c3b7e3b)

![image](https://github.com/user-attachments/assets/35f2b382-9884-46f9-9d9b-75b1e8e1cd63)

# Murmur2 Algorithm

Murmur2 is a hash function used in Apache Kafka to generate a hash value for partitioning messages across different partitions. It takes in a byte array and produces a 32-bit hash value. Kafka uses this hash value to determine the partition to which a message should be written. Murmur2 is preferred over other hash functions due to its speed and low collision rates. It is also used in other distributed systems for consistent hashing.

![image](https://github.com/user-attachments/assets/07692e65-7a12-456f-a586-543b09000e44)

![image](https://github.com/user-attachments/assets/ad074955-11d3-4a6f-90ec-5b6f96265e60)

![image](https://github.com/user-attachments/assets/62fb6556-4e1d-4494-97f8-dbba6a603663)

![image](https://github.com/user-attachments/assets/f2921f61-631f-44fe-8909-250f5cc41b22)

![image](https://github.com/user-attachments/assets/9631015f-9ba6-4d13-9209-edf841bda87c)

# Consumer Offsets
In Apache Kafka, consumer offsets are used to track the progress of a consumer group in consuming messages from one or more Kafka topics. A consumer offset is a metadata record that specifies the last message that the consumer group has successfully processed.
When a consumer group reads messages from a Kafka topic, it keeps track of the last offset that it has processed for each partition of the topic. The offset is stored in a special topic called the "__consumer_offsets" topic, which is maintained by the Kafka brokers. The consumer group periodically commits the latest offsets it has processed, so that if the consumer fails or restarts, it can resume reading from where it left off.
Kafka also provides several mechanisms for managing consumer offsets, such as automatic offset commit, manual offset commit, and checkpointing. These mechanisms provide different levels of control over how consumer offsets are managed and can be used to optimize performance and reliability based on specific use cases.

![image](https://github.com/user-attachments/assets/c99e25ad-15ff-47b3-9668-e3d3b234ca36)

![image](https://github.com/user-attachments/assets/55026134-26f2-4022-93e9-5aa511372716)

# Kafka Broker
In Apache Kafka, a broker is a core component that serves as a message broker or an intermediary between producers and consumers. A Kafka cluster is composed of one or more brokers that work together to store and replicate the data.
A Kafka broker is responsible for handling incoming messages from producers, storing them in a durable and fault-tolerant manner, and delivering them to consumers. Each broker is identified by a unique integer identifier, and it can manage multiple partitions across different topics.
When a producer sends a message to a Kafka topic, the message is initially received by one of the brokers in the cluster, which assigns it to a specific partition within the topic. The broker then replicates the message to other brokers in the cluster, ensuring that it is available for consumption by consumers.
Kafka brokers are designed to be scalable, fault-tolerant, and high-performance. They are typically deployed in a distributed configuration across multiple machines or nodes to ensure high availability and fault tolerance.
Brokers work together to form a Kafka cluster, which can scale horizontally by adding or removing brokers as needed. This allows Kafka to handle large volumes of data and support real-time data streaming applications across various industries, such as finance, e-commerce, and logistics.

![image](https://github.com/user-attachments/assets/b1bed913-e30c-4f67-b611-100bc2dd1c11)

![image](https://github.com/user-attachments/assets/f3105eab-ed53-4d36-9b40-185615f97086)

![image](https://github.com/user-attachments/assets/457f8376-2666-4a7a-8774-8fa86956754a)

# Bootstrap Server

In Apache Kafka, a bootstrap server is a configuration parameter that specifies the initial set of brokers that a Kafka client should connect to when it first starts up. It is the entry point for a Kafka client to establish a connection to the Kafka cluster.
When a Kafka client, such as a producer or consumer, starts up, it needs to know the location of at least one broker in the Kafka cluster to establish a connection. The bootstrap server is a comma-separated list of hostnames or IP addresses and their associated port numbers of Kafka brokers. The client uses this list to establish an initial connection to a broker and discover the metadata about the Kafka cluster, such as the available topics and partitions.
Once the Kafka client connects to a broker specified in the bootstrap server, it can fetch the metadata about the Kafka cluster, including the list of brokers, topics, and partitions. This information is then used by the client to determine which broker to send or receive messages to and from

# Allow consumers to fetch from closest replica

Kafka Consumers read by default from the broker that is the leader for a given partition.
In case you have multiple data centers, you run the risk of a slightly higher latency, as well as high network charges if you're being billing for cross data centers network traffic (which is the case with cloud computing platforms such as AWS).

![image](https://github.com/user-attachments/assets/ad5b09de-2480-4046-8433-f71e03914f1f)

Since Kafka 2.4, it is possible to configure consumers to read from the closest replica. This may help improve latency, and also decrease network costs if using the cloud.

![image](https://github.com/user-attachments/assets/bec2187d-8b8d-4b64-9a03-53e8df557cc5)


 
 
 
 

 
 
 
 
 

 

 

 

 
 

 

