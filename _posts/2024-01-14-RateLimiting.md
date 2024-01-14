---
layout: single
title: "Rate Limiting"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Rate Limiting

### Definition

- **Rate limiting is a setting of some sort of threshold** on certain operations, past which these operations will return errors.
- This act is used to manage data streams and control excessive requests to systems or applications.

### DoS Attack

- **DoS(Denial-Of-Service) Attack** is a type of network attack.
- The attack seeks to disrupt a system by flooding it with an overwhelming number of requests.
- This attack is now quite common, and can be effectively defended against using techniques like Rate Limiting.

### DDoS Attack

- **DDoS (Distributed Denial-Of-Service) Attack** is an enhanced type of network attack that builds upon the principles of a DoS attack.
- DDoS (Distributed Denial-Of-Service) attacks are challenging to distinguish and block because they involve simultaneous requests from multiple distributed computers.
- As the attack occurs through various paths, it can easily bypass security systems, necessitating more complex defense strategies.

### Redis

- Redis, a database server known for its rapid read/write capabilities and key-value storage model.
- In a Rate Limiting scenario, Redis is utilized as a caching solution to track and limit requests made to the server by each host.
