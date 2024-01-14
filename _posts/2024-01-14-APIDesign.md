---
layout: single
title: "API Design"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## API Design

### What is API?

- **API (Application Programming Interface) is a set** of protocols or tools that enable interaction between different software or systems.
- Simply put, an API provides a way for one program to access and use the functions or data of another program.
- It allows developers to easily implement complex functionalities and connect various services or applications together.

### What questions of API Design in System Design Interview?

- Design part of the Twitter / design Stripe
- Add a new function of the application
- Need to disambiguate the problem statement:
  - What part of Twitter/Stripe are we designing?
  - What functionality do we really want to support?
  - How much scale does the system have?
  - What regions are we gonna be supporting?

### What questions of API Design?

- Design the Twitter API / Design the Stripe API
- Need to clarify like:
  - What part of Twitter/Stripe are we designing his API for?
  - Are we just designing the API that supports the functionality on the homepage of Twitter?
  - Is it for the trending/settings tab?
  - Who's gonna be consuming our API?

### Tips for API Design

- Lots of conversation with the Interviewer: They’ll give you a bunch of criticism, constructive criticism. That feedback will help to make a decision.
- Create the Outline: like entities what I need.(e.g., id, customer_id, amount, currency, status, resources)
- Normally **CRUD operations** often serve as the bedrock of a functioning system and therefore find themselves at the core of many APIs.

### 3 Good Exercise of preparing the API Design Interview

1. Go through the API design interview questions(Uber API design question or the Reddit API design question): This will give you the best idea of what to actually expect in an API design interview. You can see how an API design interview goes from start to finish.
2. Go online to pick your favorite product or service that has a publicly available API and to look through their API documentation: This is the best way that you can get clear visibility into a production grade, publicly available API.
3. After doing two exercises, try to ask yourself. “How would you design that API?”
