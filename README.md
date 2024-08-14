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
