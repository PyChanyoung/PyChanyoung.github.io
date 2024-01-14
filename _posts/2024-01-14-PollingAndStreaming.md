---
layout: single
title: "Polling And Streaming"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Polling And Streaming

### Definition

- Polling and Streaming are the data transmission methods to make sure the data is not too stale.

### Polling

- The client sends data requests to the server at set intervals.
- Each request is used to check the latest status of the server.
- Network usage is predictable, allowing for efficient traffic management.
- There may be limitations in real-time data updates.
- This method can potentially use more network resources than necessary.

### Streaming

- Client and Server have a long-lived connection called ‘Socket’.
- In a socket, client and server have real time data transmission.
- This feature ensures that data is always up-to-date.
- Streaming continuously consumes network bandwidth to maintain the connection.
- Real-time data transmission can impose a continuous load on the server, and this burden can increase significantly as more clients connect.
