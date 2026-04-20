

# CSC494 IoT AI Learning

## Topic 1

## Linux, Docker, Networking, Reverse Proxy, and Cloudflare Tunnel for Secure Remote Access

Ryan Arnzen

---

## Why I Chose This Topic

This topic became one of the most important parts of my project because remote access was one of the hardest problems to solve.

I needed a way to let users reach the services from outside my home network without exposing the server to unnecessary risk.

---

## What AI Helped Me Learn

AI helped me learn:

- how to set up an Ubuntu server
- how to install and deploy containers with Docker
- what a reverse proxy does
- how domain names connect to services
- the difference between direct port exposure and proxy-based routing
- what Cloudflare Tunnel does
- how internal Docker networking works
- why hostname-based routing matters for multiple services

---

## My Understanding In My Own Words

Before this project, I only had a basic understanding of Linux server setup and remote access.

After working through the setup, this is my understanding of the system:

- Ubuntu Server gives me the base operating system to host the project
- Docker lets me run services in separate containers
- Cloudflare Tunnel acts like a secure bridge from the public internet to my server
- Nginx Proxy Manager acts like a traffic director that sends requests to the correct container
- Docker networking lets my containers talk to each other internally without exposing everything directly on my LAN
- That means users can type a domain name, and the request gets forwarded safely to the correct app

---

## Why This Matters

Without this topic, my project would have stayed local only.

Learning this topic made it possible to:

- build the server on Ubuntu
- deploy services in Docker containers
- access Nextcloud externally
- access Plex externally
- avoid opening router ports directly
- use domain names instead of raw local IP addresses
- make the project feel like a real hosted platform instead of just a local experiment

---

## My Project Example

In my final setup:

- Ubuntu Server hosts the system
- Docker runs the services
- `cloud.arnzenserver.org` routes to Nextcloud
- `media.arnzenserver.org` routes to Plex
- Cloudflare Tunnel handles the secure outside connection
- Nginx Proxy Manager forwards the request to the correct container
- Docker networking keeps the services connected internally
- This turned separate containers into one working platform

---

## What Was Confusing At First

The hardest parts were:

- learning Linux server setup well enough to host services
- understanding Docker container deployment
- understanding reverse proxy vs direct access
- figuring out why a domain could load the wrong page
- learning the difference between LAN access and public access
- separating DNS problems from proxy problems
- understanding how multiple services can share one public entry path

---

## What I Understand Now

- Ubuntu Server hosts the platform
- Docker runs each service in a separate container
- a user visits a public subdomain
- Cloudflare Tunnel receives the request
- the request reaches Nginx Proxy Manager
- Nginx checks the hostname
- the request is forwarded to the correct Docker container
- the user sees the correct service

That is the main idea I learned from this topic.

---

## Why This Was a Good AI Learning Topic

This topic shows real AI-supported learning because:

I used AI to:

- ask follow-up questions
- troubleshoot mistakes
- compare design choices
- understand why something failed
- test my understanding before applying the changes
- learn how the server, containers, and networking pieces fit together

Then I implemented the setup myself and verified results on the system.

---

## Final Reflection

The most helpful thing I learned was that secure remote access is not as simple as opening a program to the internet.

It is a series of components that each have a specific job:

- Ubuntu Server hosts the environment
- Docker isolates and runs the services
- DNS identifies where traffic should go
- the tunnel carries the request securely
- the reverse proxy routes the request
- Docker networking connects the services internally

Once I understood the roles separately, the project made much more sense.
