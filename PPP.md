# Project Plan Presentation (PPP) – Smart Home Media System (IN PROGRESS NOT FINAL)
CSC 494 – Ryan Arnzen

---

## 1) Project Goal

Build a self-hosted home infrastructure server on Ubuntu Server that provides:

- Personal cloud storage (Nextcloud)
- Centralized media storage/management
- Secure remote access without exposing open ports
- A foundation for monitoring, security hardening, and future smart-home expansion

---

## 2) Problem Domain

Many home users rely on multiple third-party services for storage and media that:

- cost money over time
- reduce privacy/control
- limit customization
- spread data across platforms

This project consolidates storage + services into a single secure home server.

---

## 3) Scope

### MVP (Initial Scope)
- Ubuntu Server installed and stable
- Docker installed and used for services
- Nextcloud deployed and accessible on the local network
- Secure remote access configured via Cloudflare proxy/tunnel + domain

### Future Expansion (Later Phases)
- Monitoring/logging dashboards
- Security hardening improvements (firewalls, auth, TLS, container isolation)
- Media ingestion workflows (ex: DVD → files → organized storage)
- Additional self-hosted services

---

## 4) Planned Features

- Ubuntu Server host
- Docker-based deployment and management
- Nextcloud file storage/sync/sharing
- Cloudflare proxy/tunnel remote access
- Domain + DNS management (Namecheap)
- Basic monitoring and system health tracking
- Media ingestion/organization workflows (future)

---

## 5) High-Level Architecture

User Devices (TV / Phone / Laptop)
→ Cloudflare Proxy / Tunnel
→ Ubuntu Server
→ Docker Containers (Nextcloud + services)

(Architecture diagram will be added to `/docs/architecture/`.)

---

## 6) Schedule & Milestones

### Sprint 1 – Foundations
- Ubuntu Server setup
- Docker installed/configured
- Repo setup + documentation baseline

### Sprint 2 – Core Services + Access
- Deploy Nextcloud
- Configure storage
- Configure domain + Cloudflare proxy/tunnel access

### Sprint 3 – Monitoring + Security
- Add monitoring/logging tools
- Harden server/container security
- Document baseline reliability checks

### Sprint 4 – Media + Polish
- Media ingestion workflows (as time allows)
- Testing + documentation cleanup
- Final demo preparation

---

## 7) Metrics (Burndown + Progress)

These metrics will be updated weekly on the Canvas Progress page.

### Burndown
- Features: **__ / __ complete**  ( __% )
- Requirements: **__ / __ complete** ( __% )

### Tests (counts)
- Acceptance tests: __
- Integration tests: __
- Unit tests: __

### LoC (Lines of Code)
- This week: +__
- Total: __

---

## 8) Learning with AI Topics

This project is paired with a Learning-with-AI repository. AI is used as a learning assistant
(explanations, troubleshooting, research) while all implementation is performed manually.

### Topic 1 (Strong fit): Server & IoT Security
- Securing Ubuntu Server
- Securing Docker containers
- Firewalls, TLS, authentication
- Secure ESP32 → server communication (future)

### Topic 2 (Strong fit): Monitoring, Logging, & Anomaly Detection
- Monitoring concepts (Prometheus/Grafana style tools)
- Log analysis
- Detecting abnormal behavior (temps, failures)
- Alerting concepts

---

## 9) Links

- **Project Repo:** https://github.com/RyArnz/csc494-smart-media-server  
- **Learning with AI Repo:** https://github.com/RyArnz/csc494-iot-ai-learning  
- **Canvas Project Page:** https://nku.instructure.com/courses/88152/pages/individual-project-ryan-arnzen  
- **Canvas Progress Page:** https://nku.instructure.com/courses/88152/pages/individual-progress-ryan-arnzen
