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

Murmur2 Algorithm
Murmur2 is a hash function used in Apache Kafka to generate a hash value for partitioning messages across different partitions. It takes in a byte array and produces a 32-bit hash value. Kafka uses this hash value to determine the partition to which a message should be written. Murmur2 is preferred over other hash functions due to its speed and low collision rates. It is also used in other distributed systems for consistent hashing.
 
 
 
 
 

 

 

 

 
 

 

