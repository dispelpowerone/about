# Text Embeddings Search Project

## Introduction

The Text Embeddings Search Project aimed to develop a web search subsystem
capable of real-time retrieval of the best matching web pages for a given
search query using text embeddings similarity. This subsystem was designed
to enhance overall web search ranking quality, particularly for long-tail,
low-frequency queries.

## My role

In this project, I was responsible for designing and implementing the storage
service. This service was capable of indexing vast amounts of pre-calculated
text embeddings and retrieving the best matches in real-time for a given text
embedding.

## Technologies used

* **Python**: For embeddings indexation and deployment were developed Python
scripts and C++ command-line tools.
* **HDFS**: Hadoop HDFS was used to store and distribute the index across
the servers.
* **C++ and Annoy Library**: Implemented the main search microservice in C++
using the Annoy library for the index layer.
* **Linux Huge pages (HugeTLB)**: Enabled Linux Huge pages on searches servers
to improve performance stability.
* **Load balancing/service discovery/sharding**: Developed a proxy-shard
microservice in C++ to manage search instances discovery, load balancing,
and results aggregation due to dataset sharding.
* **etcd**: Used etcd for service discovery to ensure efficient coordination
between proxy instances and search services.

## Team

The project team consisted of approximately 5-7 members.
Two developers, including myself, focused on the microservices implementation.
The remaining team members were working on text embeddings computation and
web search ranking improvements.
