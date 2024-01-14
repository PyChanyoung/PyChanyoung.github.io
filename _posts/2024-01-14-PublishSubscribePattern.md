---
layout: single
title: "Publish/Subscribe Pattern"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Publish/Subscribe Pattern

### Definition

- **The Publish/Subscribe Pattern**, also known as **'pub/sub pattern'**, **'pub/sub model'**, or simply **'pub/sub'**, **is a paradigm** used in the processing of streaming data. This pattern focuses on data distribution and asynchronous communication, making it highly useful in large-scale distributed systems.
- Pub/Sub involves several entities: Publisher (=Server), Subscriber (=Client), Topic, and Message.

### Entities

- **Publisher**: Publishes data (=Message) to a **Topic**. The Publisher issues messages without concern for who will receive them.

- **Topic**: Acts as a central point where messages from Publishers are received and organized. Topics can temporarily store messages, and in some systems, messages are kept in persistent storage depending on the system's design and requirements.

- **Subscriber**: subscribe to one or more Topics and receive messages posted to these Topics. Subscribers can choose specific Topics to receive the information they need.

### Storage

- A Topic can temporarily store messages, and in some systems, messages may be stored in persistent storage. This depends on the design and requirements of the system.

### Asynchronous

- Data transfer is asynchronous, allowing Subscribers to receive data from Topics whenever they need, without the need to be always online.
