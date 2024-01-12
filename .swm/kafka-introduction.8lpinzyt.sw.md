---
title: Kafka Introduction
---
Kafka is a distributed system. Read this article for complete understanding of kafka in a nutshell. <https://softwaremill.com/what-problems-does-kafka-solve-in-distributed-systems/>

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2Fabe097ce-f7d0-4973-90c0-f832bdff2d4b.png?alt=media&token=ec4ea7ef-1b82-46fc-8bef-2070405f8325)

# Kafka Cluster

Since kafka is a distributed system, it acts as a cluster. A kafka cluster contains set of brokers. A cluster has a minimum of 3 brokers.

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2Ffe0cb2f3-1686-48ce-9f0f-91ddf8930601.png?alt=media&token=2a58dcc2-5632-4e10-9916-a8b8f0efbc87)

# Kafka Broker

A broker is a kafka server. It's just a meaningful name given to the kafka server. It acts as a broker between producer and consumer.&nbsp;

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2F630db845-593b-4433-901c-2dba69365046.png?alt=media&token=5daee04a-877a-48a6-9a8c-82ac327d5bb4)

# Kafka Topic

We learned that producer sends data to the kafka broker. Consumer consumes data from the kafka broker. Which data? We need to have some identification mechanism to request data from a broker. There comes a notion of Topic.&nbsp;

- Topic is like a table in database or folder in a file system.
- Topic is like a category in the kafka broker which categories the messages.
- In topic, it stores the records in a sequential manner.
- Topic is identified by the name.
- You can have any number of topics.
- Data can be text, string, byte array, JSON etc.

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2F72d24c4b-2335-450a-9571-103b56ef7a7e.png?alt=media&token=eb3ea3fb-b2b1-4e36-a32a-86470a908111)

# Partition

Kafka Topics are divided into number of Partitions, which contains records in an unchangeable sequence.

> Kafka broker will store the messages for a Topic. But the capacity of data can be enormous and it may not be possible to store in a single computer. Therefore it will be partitioned into multiple parts and distributed among multiple computers, since Kafka is a distributed system.

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2Fb6469925-1798-4b90-adb7-5bc3e8843481.png?alt=media&token=96bfccaf-514f-4692-98ff-2e6637c8ba6f)

# Offsets

Offset is a sequence of ids given to messages as the arrival at a partition. Once the offset is assigned it will never be changed. The first message gets an offset 0. The next message gets an offset 1 and soon.

![](https://firebasestorage.googleapis.com/v0/b/swimmio.appspot.com/o/repositories%2FZ2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0%2F836b8168-e38e-45ea-9a29-5710c2e468e8.png?alt=media&token=4cffb4ea-1746-498c-bff5-d673de41134b)

<SwmMeta version="3.0.0" repo-id="Z2l0aHViJTNBJTNBa2Fma2EtaXElM0ElM0FmYXJvb3F0ZXh0" repo-name="kafka-iq"><sup>Powered by [Swimm](https://app.swimm.io/)</sup></SwmMeta>
