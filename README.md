# CSC 494 Learning with AI

## Overview

This repository documents how I used AI as a learning assistant during the development of my Smart Home Media Server project. The purpose of this repo ie to show how AI helped me learn technical topics, apply them to my system, and explain what how I understand it.

AI helped me break down concepts, compare tools, troubleshoot technical issues, and understand how multiple technologies worked together. I used that information to test configurations, build the system, verify results, and document what I learned. This made AI useful as a support tool for deeper understanding rather than just a shortcut.

The Smart Home Media Server project itself combines remote media streaming, public cloud storage, system monitoring, and Raspberry Pi-based physical telemetry into one self-hosted platform. Because of that, the two main Learning with AI topics in this repository are closely tied to the most important technical challenges in the project.

---

## Why This Repository Matters

This repository shows how AI contributed to my learning process in a practical way. Instead of only asking AI for final answers, I used it to understand systems, fix problems, and build working solutions.

This repo demonstrates:
- how AI supported my understanding of Linux, Docker, networking, monitoring, and Raspberry Pi integration
- how I applied that knowledge in a real project instead of leaving it theoretical
- how I interpreted the topics in my own words after testing them myself
- how AI can be useful for learning when combined with implementation, troubleshooting, and reflection

---

## Related Project

This repository is connected to my Smart Home Media Server project.

**Main project repository:**  
[CSC494 Smart Media Server](https://github.com/RyArnz/csc494-smart-media-server)

That project includes the actual server platform, services, documentation, monitoring setup, and Raspberry Pi integration that these learning topics are based on.

---

## Topic 1

## Linux, Docker, Networking, Reverse Proxy, and Cloudflare Tunnel for Secure Remote Access

This topic focuses on the infrastructure side of the project. It became one of the most important areas I had to learn because remote access was one of the hardest parts of the build. It was not enough to make services run locally. I needed to understand how to build the server environment, deploy applications in containers, and make services accessible from outside my home network in a secure and organized way.

AI helped me understand how to set up an Ubuntu server, how Docker containers are deployed and managed, and how networking concepts such as DNS, reverse proxying, port forwarding, and tunneling all fit together. Before this project, I had only a basic understanding of remote access. Through AI, I was able to learn the different roles of the system.

This is my understanding of the system:
- Ubuntu Server provides the base environment for hosting the platform
- Docker allows each major application to run in its own isolated container
- Cloudflare Tunnel acts like a secure bridge between the public internet and my private server
- Nginx Proxy Manager acts like a traffic director that routes incoming requests to the correct service
- Docker networking allows containers to communicate internally without exposing every service directly to the local network


### Topic 1 Relevance to the Project

This topic was directly applied in the final system by allowing:
- external access to Plex
- external access to Nextcloud
- domain-based routing through subdomains
- secure service access through Cloudflare Tunnel
- service routing through Nginx Proxy Manager
- containerized deployment on Ubuntu Server using Docker

### What I Learned from Topic 1

I learned how to set up an Ubuntu server and deploy containerized services with Docker. I also learned networking concepts such as port forwarding, reverse proxying, DNS, and tunneling. AI helped me understand how Cloudflare Tunnel, Nginx Proxy Manager, and Docker networking work together to get outside traffic to the correct service.

---

## Topic 2

## Monitoring with Prometheus, Grafana, and Raspberry Pi Health Indicators

This topic focuses on observability and system awareness. Once the core services were working, the next step was monitoring it's peroformance. I didn't want the system failing unexpectedly so I used AI to build a system that could be monitored, measured, and displayed in several ways.

AI helped me understand how Prometheus, Grafana, exporters, and Raspberry Pi hardware could work together as one monitoring system. Before this project, I mostly thought of monitoring as dashboards and numbers in the corner of a screen. Through AI explanations and troubleshooting, I learned that we can use the data given to use from monitoring to control our system and determine what parts need upgrading.

I now understand the monitoring system like this:

- Prometheus collects and stores metric data over time
- Grafana turns that data into readable dashboards and visualizations
- `node_exporter` provides host-level system data such as CPU, RAM, disk usage, and uptime
- `cAdvisor` provides container-level metrics for Docker services
- Raspberry Pi LEDs can translate monitoring conditions into simple physical status indicators

### Topic 2 Relevance to the Project

This topic was directly applied in the final system by allowing:

- collection of server health metrics
- collection of Docker container metrics
- visualization of system performance in Grafana
- observation of CPU, RAM, disk usage, and uptime
- observation of container count and per-container resource usage
- Raspberry Pi LED indicators for physical server-health feedback

### What I Learned from Topic 2

I learned how to set up monitoring so it is more than just looking at graphs. Each tool has its own role in tracking system health. AI helped me understand how Prometheus collects metrics, how Grafana displays them, how exporters provide the data, and how Raspberry Pi LEDs can turn that data into a simple physical status display.

---

## How AI Helped Me Learn

I used AI consistently to:
- ask follow-up questions about unfamiliar concepts
- compare technologies and design choices
- troubleshoot Linux, Docker, and networking issues
- understand why certain configurations failed
- learn how monitoring tools fit together
- generate example code that I could review, test, and adapt
- organize my understanding into slides and documentation

The most important part of the process was that I still had to test the configurations myself. AI could explain ideas and suggest solutions, but I had to apply them, verify them, and decide what actually worked for my system.

---


## Marp Slides

- Topic 1 PDF: [link]
- Topic 2 PDF: [link]
