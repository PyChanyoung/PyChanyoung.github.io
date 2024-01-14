---
layout: single
title: "Security And HTTPS"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Security and HTTPS

### Man-In-The-Middle Attack (MITM attack)

- This is an attack where a hacker intercepts and potentially alters the communication packets between a client and a server.

### Symmetric Encryption

- This type of encryption uses a single key for both encrypting and decrypting data. This key must be known to all parties involved in the communication.

### Asymmetric Encryption

- In this encryption method, two keys (a public key and a private key) are used for encryption and decryption. Data encrypted with the public key can only be decrypted with the corresponding private key.

### AES (Advanced Encryption Standard)

- It is a widely used international encryption standard that utilizes three symmetric-key algorithms: AES-128, AES-192, and AES-256.

### HTTPS(Hyper-Text Transfer Protocol Secure)

- An extension of HTTP enhanced for security. It requires servers to have trusted SSL certificates and uses the Transport Layer Security (TLS) protocol, built on top of TCP, to encrypt data.

### TLS(Transport Layer Security)

- A security protocol over which HTTP runs to achieve secure online communication.

### SSL Certificate

- A digital certificate issued to a server by a certificate authority. It includes the server's public key and is used in the TLS handshake process in an HTTPS connection. SSL certificates are crucial for confirming the ownership of the public key and defending against man-in-the-middle attacks.

### Certificate Authority

- A trusted entity that signs digital certificates—namely, SSL certificates that are relied on in HTTPS connections.

### TLS Handshake

- The TLS Handshake in an HTTPS connection, which establishes a secure communication channel, operates in the following steps:

  1. Client Hello: The client sends a "Client Hello" message to the server. This message contains the TLS version supported by the client, available cryptographic algorithms, and a random byte string for security.

  2. Server Hello: The server responds with a "Server Hello" message. It includes the TLS version and cryptographic algorithm selected by the server from the client's options, and another random byte string.

  3. Certificate Exchange: The server sends its SSL certificate to the client. This certificate contains the server's public key, enabling the client to verify the server's legitimacy.

  4. Key Exchange: The client uses the server's public key to encrypt a message, known as the Premaster Secret Data, and sends it to the server.

  5. Secret Agreement: The server generates a session key using the Premaster Secret and strings from the Hello messages.

  6. Final Agreement: Both the client and server send messages confirming the start of an encrypted session. Subsequent communication is encrypted using the session key.
