---
layout: single
title: "Logging And Monitoring"
categories: SystemDesign
tag: [SystemDesign, Fundamental]
toc: true
toc_sticky: true
toc_label: Syllabus
author_profile: false
---

## Logging And Monitoring

### Definition

- **Logging and Monitoring are solutions** for detecting issues and tracking the status of systems, respectively.

### Logging

- Logging is a process to collect and store information about events.
- All logs are aggregated to some databases - central logging solution(e.g., AlgoExpert uses Stackdriver for a logging solution), providing useful detailed information about the activity of a system or application, errors, transactions, which is essential for analyzing and debugging.

### Monitoring

- Monitoring is a tool for visualizing a system's key metric.
- Key metrics depend on the system. For instance, one important key metric for AlgoExpert is Code Execution per Hour.

### Alerting

- The process through which system administrators get notified when critical system issues occur.
- Alerting can be set up by defining specific thresholds on monitoring charts, past which alerts are sent to a communication channel like Slack.
