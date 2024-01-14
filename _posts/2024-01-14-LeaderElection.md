---
layout: single
title: "Leader Election"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Leader Election

### Definition

- **Leader Election is the process** used in a distributed system that elects the **leader** among the servers in a cluster to entrust primarily services.
- Other servers in a cluster stand by while the leader works. If the Leader is down, elect another leader through the election process.

### Consensus Algorithm

- This algorithm enables the server group in a distributed system to reach consensus on that single data value like ‘Leader’.
- These consensus guarantee the consistency and integrity of the system.

### Paxos & Raft

- These two algorithms are the most famous consensus algorithms used in distributed systems.
  - Paxos: This consensus algorithm guarantee the data synchronization and consistence state.
  - Raft: Raft is a consensus algorithm that ensures consistent data and reliable leader election in distributed systems, valued for its simplicity and effectiveness.

### Etcd

- Etcd is a key-value store that guarantees strongly consistent and highly available using Raft consensus algorithm .

### ZooKeeper

- ZooKeeper is a strongly consistent, highly available key-value store. It's often used to store important configurations or to perform leader elections.
