# CSC 494 Learning with AI

## Overview

This repository documents how AI was used as a learning assistant throughout my Smart Home Media Server project. The goal of this repo is not just to show AI-generated information, but to show how I used AI to understand technical topics, apply them in a real system, and explain them in my own words.

During this project, AI helped me learn about Linux server setup, Docker deployment, networking, reverse proxy design, Cloudflare Tunnel, monitoring, observability, and Raspberry Pi integration. I used AI to ask questions, compare approaches, troubleshoot issues, and better understand how each part of the system fit together. After that, I tested and verified the results on the project.

This learning process is tied directly to the development of my Smart Home Media Server, which combines remote media streaming, cloud storage, live monitoring, and Raspberry Pi-based physical telemetry into one self-hosted platform.

---

## Topic 1

### Linux, Docker, Networking, Reverse Proxy, and Cloudflare Tunnel for Secure Remote Access

This topic focuses on the infrastructure side of the project. AI helped me understand how to set up an Ubuntu server, deploy containerized services with Docker, and connect multiple services together using networking and reverse proxy tools.

I learned how port forwarding, reverse proxying, DNS, and tunneling all play different roles in secure remote access. Before this project, I only had a partial understanding of how outside traffic reaches a service running on a private machine. Through AI-supported learning and troubleshooting, I learned how Cloudflare Tunnel can securely bring traffic into the network, how Nginx Proxy Manager can route traffic to the correct container, and how Docker networking lets containers communicate internally.

This topic became one of the most important parts of the project because remote access was one of the hardest problems to solve. Without this knowledge, the project would have remained local only.

---

## Topic 2

### Monitoring with Prometheus, Grafana, and Raspberry Pi Health Indicators

This topic focuses on visibility into system health. AI helped me understand how to move beyond simply getting services running and instead build a system that can be monitored over time.

I learned how Prometheus collects and stores metrics, how Grafana turns those metrics into dashboards, how exporters like `node_exporter` and `cAdvisor` provide host and container data, and how a Raspberry Pi can be used to display server health. AI also helped with code generation for python files.

This topic helped me understand the difference between host-level monitoring and container-level monitoring. It also showed me how monitoring can lead to better troubleshooting, better performance awareness, and possibly future automation. Instead of guessing how the system is doing, I can now measure it and react to real data.

---

## What I Learned

### Topic 1 Reflection

I learned how to set up an Ubuntu server and deploy containerized services with Docker. I also learned networking concepts such as port forwarding, reverse proxying, DNS, and tunneling. AI helped me understand how Cloudflare Tunnel, Nginx Proxy Manager, and Docker networking work together to make secure remote access possible.

### Topic 2 Reflection

I learned how to set up monitoring so it is more than just looking at graphs. Each tool has its own role in tracking system health. AI helped me understand how Prometheus collects metrics, how Grafana displays them, how exporters provide the data, and how Raspberry Pi can use prometheus data to display system health.

---

## Marp Slides

- Topic 1 PDF: [link]
- Topic 2 PDF: [link]

---

## Reflection

AI was most helpful when I used it as a guide instead of a replacement for my own work. It helped speed up troubleshooting, explain unfamiliar concepts, compare design choices, organize documentation, and generate code. At the same time, I still had to test every configuration, verify the behavior of the real system, and decide what actually worked for my project.

---

## Related Project Repository

- Smart Home Media Server: https://github.com/RyArnz/csc494-smart-media-server
