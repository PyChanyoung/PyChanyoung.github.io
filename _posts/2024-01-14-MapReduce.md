---
layout: single
title: "MapReduce"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## MapReduce

### Definition

- **MapReduce is indeed a data processing model** designed for handling large-scale data sets. It emerged as a response to the challenges of processing increasingly larger datasets that could not be managed effectively through traditional vertical scaling methods.
- In the early 2000s, Google engineers recognized the limitations of existing data processing methods due to the rapidly growing size of datasets. This realization led to the development of a new approach.
- **Jeffrey Dean** and **Sanjay Ghemawat** authored a seminal white paper in 2004 titled **["MapReduce: Simplified Data Processing on Large Clusters."](https://research.google/pubs/mapreduce-simplified-data-processing-on-large-clusters/)**
- This paper introduced the MapReduce model to the world and detailed how it could efficiently process large amounts of data using a distributed and parallel architecture. The paper became a foundational text in the field of big data processing and inspired numerous implementations and adaptations in various big data technologies.
- A MapReduce job is comprised of **3 main steps**:
  - **Map**: The map function accesses various chunks of the dataset in a distributed system, **transforming them into intermediate key-value pairs**.
  - **Shuffle**: **Reorganizes** the intermediate key-value pairs such that pairs of the same key are routed to the same machine in the final step.
  - **Reduce**: The reduce function on the newly shuffled key-value pairs and **transforms them into more meaningful data**.

### Distributed File System (DFS)

- **A DFS is an abstraction** over a (usually large) cluster of machines that allows them to act like one large file system.
- A DFS guarantees that **Distributed storage**, **Replication and High Availability**, **Scalability**, **Transparency**, **Reliability and Fault tolerance**.
- 2 Famous DFS are the **Google File System** and **Hadoop**.

### Hadoop

- A popular, open-source framework that supports MapReduce jobs and many other kinds of data-processing pipelines. Its central component is HDFS (Hadoop Distributed File System), on top of which other technologies have been developed.
