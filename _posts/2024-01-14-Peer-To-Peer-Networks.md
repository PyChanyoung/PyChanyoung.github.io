---
layout: single
title: "Peer To Peer Networks"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Peer-To-Peer Networks

### Definition

- Peer-To-Peer Networks is a **Decentralization** Network Solution.
- In P2P Networks, Every computer is called **Peer**.
- When one peer sends a large file, it is divided into small pieces called **Chunks** before being sent to another peer.
- Once a peer receives a chunk, it **simultaneously** starts sharing that chunk with other peers.
- This sequence of actions resembles the way **Gossip spreads**, simultaneously propagating the file across the network. This reduces the load on the network and enables faster file transmission.

### Gossip Protocol

- Probabilistic Information Dissemination: The Gossip Protocol spreads information **probabilistically**, without relying on a central data source.
- Rumor-like Mechanism: This mechanism is similar to the way rumors spread among people, hence the name "Gossip Protocol."
