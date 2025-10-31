[العربي](./12-site-reliability-engineering_ar.md)

# <a name="-12-site-reliability-engineering-sre"></a>🛡️ Chapter 12: Site Reliability Engineering (SRE)

## 1. What is it?

Site Reliability Engineering (SRE) is an engineering discipline, coined by Google, that aims to apply software engineering principles to infrastructure and operations problems. The primary goal is to create highly reliable and scalable software systems.

The core idea of SRE is: "Treating operations as a software problem." Instead of manually solving problems repeatedly, an SRE writes software and systems to automate the solutions.

> The famous quote from Google: "SRE is what happens when you ask a software engineer to design an operations team."

## 2. What does the specialist do?

The primary goal of an SRE is to ensure that a service meets its defined reliability targets. Their work is a delicate balance between proactive engineering and reactive operations:

 * Proactive Engineering (more than 50% of their time):
     * Writing software to automate operational tasks.
     * Improving system architecture to increase reliability.
     * Building advanced monitoring systems.
     * Performing Capacity Planning to predict future growth.

 * Reactive Operations (less than 50% of their time):
     * Responding to incidents and outages (being "On-call").
     * Managing outages as they occur.
     * Writing "Post-mortems" to learn from mistakes and prevent them from recurring.

## 3. Sub-domains

 * Observability: Building systems that provide deep insight into system health.
 * Incident Response: Leading recovery efforts during outages.
 * Capacity Planning: Predicting future growth and ensuring sufficient resources are available.
 * Automation: Building software to eliminate "Toil."

## 4. Expanded Key Concepts

These are the concepts that distinguish the SRE philosophy:

 * `SLI (Service Level Indicator)`: A quantitative measure of some aspect of the service.
     * Example: The percentage of successful requests (that return a 200 code).

 * `SLO (Service Level Objective)`: A target value for an SLI. This is an internal goal for the team.
     * Example: "99% of homepage requests should have a latency of less than 300ms."

 * `SLA (Service Level Agreement)`: A legal contract with a customer that includes consequences (like financial compensation) if SLOs are not met.
     * Note: SREs focus on meeting SLOs to ensure SLAs are met.

 * `Error Budget`: The flip side of an SLO. If your SLO is 99.9% availability, your error budget is 0.1%. This is the amount of "acceptable" failure.
     * The key idea: The error budget is treated as a resource that can be "spent." If the budget is full, the team can launch new features quickly and take risks. If the budget is depleted, all new feature launches are frozen, and the team must focus exclusively on improving reliability. This creates a data-driven balance between innovation and stability.

 * `Toil`: Any manual, repetitive, automatable, tactical work that lacks long-term value. The primary goal of an SRE is to eliminate Toil by writing automation software.

 * `Post-mortem`: A detailed document that records an outage incident, its impact, the actions taken, the root cause, and follow-up steps to prevent recurrence. The core principle here is to be Blameless. The focus is on fixing systems, not blaming people.

## 5. Expanded Tools & Technologies

The tools are very similar to DevOps tools, but the application method differs:
 * Observability: Prometheus, Grafana, Jaeger (for Tracing).
 * Automation and Scripting: Python, Go, Bash.
 * Infrastructure: Kubernetes, Terraform, Ansible.
 * Incident Management: PagerDuty, Opsgenie.
 * Chaos Engineering: Gremlin, Chaos Monkey (tools that intentionally inject failure into the system to test its resilience).

## 6. In-Depth Workflow

Project: An SRE team is responsible for the critical "Checkout" service on an e-commerce site.

 1. Defining Reliability (SLOs): The SRE team works with the product manager to define what "reliability" means for this service. They agree on two objectives:
     * Availability SLO: 99.95% of requests must be successful over a 28-day period.
     * Latency SLO: 99% of requests must complete in less than 250ms.
 2. Calculating the Error Budget: The 99.95% availability target gives them an error budget of 0.05%, which is about 21 minutes of permissible downtime every 28 days.
 3. Implementing Monitoring (SLIs): The team sets up Prometheus to collect metrics from the service and builds a Grafana dashboard to track the SLIs and the remaining error budget in real-time.
 4. Incident Response: One of the SREs is "On-call." Suddenly, an alert fires: "Error rate has exceeded 5% for 5 minutes!" The engineer receives an alert on their phone from PagerDuty. They join a video call, declare themselves the "Incident Commander," and start diagnosing the problem. They discover that a recent code deployment caused a memory leak. They trigger a rollback to the previous version. The incident is resolved.
 5. Post-mortem: The next day, the engineer leads a blameless Post-mortem meeting. The team documents the incident timeline, impact, and root cause. They come up with action items: "Add a new alert for memory consumption" and "Improve the CI pipeline to include a load test that could have caught this leak before deployment."
 6. Engineering to Eliminate Toil: The team notices they spend a lot of time manually creating test databases for developers. They spend the next Sprint writing a Python tool that completely automates this process, turning a 30-minute manual task into a 30-second command.

## 7. Common Job Roles

 * Site Reliability Engineer (SRE)
 * Systems Engineer (SRE Focus)
 * Observability Engineer

## 8. A-Z Glossary
<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Availability`** | The percentage of time a service is available and functioning correctly. |
| **`Blameless Post-mortem`** | A post-incident report that focuses on analyzing systemic causes of failure rather than blaming individuals. |
| **`Capacity Planning`** | The process of predicting future resource requirements to maintain service performance. |
| **`Chaos Engineering`** | The practice of experimenting on a system in production by injecting failure to test its resilience. |
| **`Error Budget`** | The amount of permissible failure based on the SLO. |
| **`Incident`** | Any unplanned event that causes an interruption or degradation in service quality. |
| **`Latency`** | The time it takes for a request to get a response. |
| **`MTTR (Mean Time To Repair)`** | The average time it takes to repair a system after a failure. |
| **`On-Call`** | The responsibility of responding to critical incidents outside of normal working hours. |
| **`Post-mortem`** | A post-incident report. |
| **`Reliability`** | The ability of a system to consistently perform its required function correctly. |
| **`SLI / SLO / SLA`** | Service Level Indicator / Objective / Agreement. |
| **`Toil`** | Manual, repetitive work that lacks long-term value. |

</details>

[⬆️ Back to Table of Contents](README.md)