CSC494 IoT AI Learning

Topic 1

Networking, Reverse Proxy, and Cloudflare Tunnel for Secure Remote Access

Ryan Arnzen

---
Why I Chose This Topic:

This topic became one of the most important parts of my project because remote access was one of the hardest problems to solve.
I needed a way to let users reach the services from outside my home network without exposing the server to unnecessary risk.

---
What AI Helped Me Learn

AI helped me learn:

- what a reverse proxy does
- how domain names connect to services
- the difference between direct port exposure and proxy-based routing
- what Cloudflare Tunnel does
- how internal Docker networking works
- why hostname-based routing matters for multiple services

---

Before this project, I only had a basic understanding of reverse access.

After working through the setup, this is my understanding of the system:

- Cloudflare Tunnel acts like a secure bridge from the public internet to my server
- Nginx Proxy Manager acts like a traffic director that sends requests to the correct container
- Docker networking lets my containers talk to each other internally without exposing everything directly on my LAN
- That means users can type a domain name, and the request gets forwarded safely to the correct app.
---
Why This Matters

Without this topic, my project would have stayed local only.

Learning this topic made it possible to:

- access Nextcloud externally
- access Plex externally
- avoid opening router ports directly
- use domain names instead of raw local IP addresses
- make the project feel like a real hosted platform instead of just a local experiment
---
My Project Example

In my final setup:

- `cloud.arnzenserver.org` routes to Nextcloud
- `media.arnzenserver.org` routes to Plex
- Cloudflare Tunnel handles the secure outside connection
- Nginx Proxy Manager forwards the request to the correct container
- Docker networking keeps the services connected internally
- This turned separate containers into one working platform.
---
What Was Confusing at First

The hardest parts were:

- understanding reverse proxy vs direct access
- figuring out why a domain could load the wrong page
- learning the difference between LAN access and public access
- separating DNS problems from proxy problems
- understanding how multiple services can share one public entry path
- At first, it all felt like the same networking issue. After working through it, I learned that each layer has a different job.
---
What I Understand Now

- A user visits a public subdomain
- Cloudflare Tunnel receives the request
- The request reaches Nginx Proxy Manager
- Nginx checks the hostname
- The request is forwarded to the correct Docker container
- The user sees the correct service
- That is the main idea I learned from this topic.
---
Why This Was a Good AI Learning Topic

- This topic shows real AI-supported learning because I did not just ask AI for definitions.
I used AI to:
- ask follow-up questions
- troubleshoot mistakes
- compare design choices
- understand why something failed
- test my understanding before applying the changes
Then I implemented the setup myself and verified result on my own system.
---
Final Reflection
The most helpful information was that secure remote access is not as simple as "opening something to the internet."
It is a chain of components that each do a specific job:
- DNS identifies where traffic should go
- the tunnel carries the request securely
- the reverse proxy routes the request
- Docker networking connects the services internally
Once I understood the roles separately, the project made more sense.
