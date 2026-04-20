

# CSC494 IoT AI Learning

## Topic 2

## Monitoring with Prometheus, Grafana, and Raspberry Pi Health Indicators

Ryan Arnzen

---

## Why I Chose This Topic:

This topic became important once the server itself was working because I realized that having services online is not the same thing as actually understanding the health of the system.

I wanted a way to observe the server, the containers, and the major services so I could see problems early instead of waiting for something to fail.

---

## What AI Helped Me Learn

AI helped me learn:

- what Prometheus does
- how Grafana uses collected metrics
- the difference between host monitoring and container monitoring
- what `node_exporter` measures
- what `cAdvisor` measures
- how monitoring data can be used for warnings and health checks
- how a Raspberry Pi could be used as a physical health display

---

Before this project, I mostly thought of monitoring as just graphs on a screen.

After working through the setup, this is my understanding of the system:

- Prometheus collects and stores metric data over time
- Grafana turns that data into dashboards that are easier to read
- `node_exporter` reports host-level system information like CPU, RAM, disk usage, and uptime
- `cAdvisor` reports container-level information like Docker CPU and memory usage
- the Raspberry Pi can turn monitored conditions into simple physical status indicators
- That means I can understand system health both from dashboards and from hardware output.

---

## Why This Matters

Without this topic, my project would only show that services run.

Learning this topic made it possible to:

- observe overall server health
- track container behavior
- measure CPU, RAM, disk, and uptime
- identify which services are consuming resources
- build a physical status display with Raspberry Pi LEDs
- create a path toward alerts, automation, and predictive maintenance

---

## My Project Example

In my final setup:

- Prometheus collects metrics from the server
- Grafana displays dashboards for those metrics
- `node_exporter` provides host statistics
- `cAdvisor` provides container statistics
- the Raspberry Pi polls health information and controls LEDs
- the LED mapping shows server status at a glance
- This turned monitoring into something I could both visualize and physically display.

---

## What Was Confusing At First

The hardest parts were:

- understanding the difference between host monitoring and container monitoring
- learning why Prometheus needed exporters
- figuring out why Grafana panels sometimes showed no data
- choosing which metrics were actually useful
- understanding how monitoring data could connect to Raspberry Pi output
- At first, all the tools felt separate. After working through it, I learned that each one fills a specific role in the monitoring pipeline.

---

## What I Understand Now

- Prometheus collects the metrics
- exporters provide the data sources
- Grafana visualizes the results
- host metrics describe the overall server
- container metrics describe each Docker application
- the Raspberry Pi gives a simple hardware-based summary
- That is the main idea I learned from this topic.

---

## Why This Was a Good AI Learning Topic

- This topic shows real AI-supported learning because I did not just ask AI for definitions.

I used AI to:

- ask follow-up questions
- troubleshoot “no data” problems
- understand what each tool was responsible for
- compare different monitoring ideas
- think through how to map health data to LEDs

Then I implemented the setup myself and verified the result on my own system.

---

## Final Reflection

The most helpful thing I learned was that monitoring is how to use one application to pull data for other programs to act on. 

I was able to design system where each part has a specific job:

- Prometheus collects and stores data
- exporters expose the data
- Grafana makes the data readable
- the Raspberry Pi makes the data visible in physical form

Once I understood the roles separately, the project felt more manageable.
