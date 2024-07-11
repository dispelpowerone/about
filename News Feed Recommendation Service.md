# News Feed Recommendation Service

## Introduction

The project started as a small MVP and grew up into recommendations feed
provider for the company's primary web page. See [here](https://mail.ru).
The idea was to design and implement a service that provides a list of news 
and blog posts for users based on available user data using ML-based ranking.

## My role

I was an architect and the main contributor to the backend.
I contributed about 70% of the core microservices:
1. Indexation microservice - to build and continusely update the dataset.
2. Recommendation core microservice - to find a list of documents
using ML ranking. My goal was to provide ML engineers with easy-to-use
abstractions for ML integtration and tuning.
3. Middle-end microsrvice to join results from several recommendation instances.
4. Gateway microservice - to format the final result, results caching,
store/restore user's session data, etc.

## Technologies used

* **C++**: The microservices were developed in C++.
* **HDFS**: Hadoop DFS was used as a primary source of data for indexation.
It also was used to store dataset backups/snapshots.
* **Kafka**: Dataset updates were sent to recommendation instances through Kafka.
* **Protobuf**: Google Protobuf was used for dataset in-memory representation
and updates transfer.
* **Aerospike**: Aerospike NoSQL storage was used to store session-related data 
and recommendations caching.

## Team

The team grew from 4 developers at the beginning to about 10-12 at the end.
Usually I developed a microservice base version from scratch myself and
later worked on it together with other engineers.
