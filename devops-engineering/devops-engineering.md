[العربي](./devops-engineering_ar.md)

# <a name="-11-devops-engineering"></a>🚀 Chapter 11: DevOps Engineering

## 1. What is it?

DevOps is a cultural philosophy, a set of practices, and tools that aim to increase an organization's speed and efficiency in delivering applications and services. The primary goal is to break down the barriers between the development team (Dev) and the operations team (Ops) through automation and collaboration, leading to a faster and more reliable software development lifecycle.

Simply put, if the software engineer builds the car and the cloud engineer builds the road, the DevOps engineer builds the "automated factory and assembly line" that moves the car from the design stage to the highway smoothly and safely.

## 2. What does the specialist do?

A DevOps engineer is the "automation expert" and "process optimizer." They don't typically write new feature code for the application, but rather build, manage, and improve the "factory" (the CI/CD pipeline) that builds, tests, and deploys the code. Their tasks include:

* Building and maintaining CI/CD pipelines: Creating fully automated systems for software delivery.
* Managing Infrastructure as Code (IaC): Using tools like Terraform to define and manage infrastructure.
* Implementing Monitoring & Logging solutions: Building systems to monitor the health of applications and infrastructure in real-time.
* Automating operational tasks: Writing scripts to automate repetitive tasks.
* Working closely with developers: Helping them improve the deployment process and solve infrastructure-related problems.

## 3. Sub-domains

* CI/CD Engineering: Specializing in building and optimizing integration and deployment pipelines.
* Infrastructure Automation: Focusing on IaC tools like Terraform and configuration management tools like Ansible.
* Site Reliability Engineering (SRE): A specific implementation of DevOps (coined by Google) that uses software engineering principles to solve operations problems. (To be explained in a future chapter).
* Platform Engineering: A new trend where a central team builds an "internal developer platform" (IDP) that provides self-service tools for developers, abstracting away the complexities of DevOps and the cloud.

## 4. Expanded Key Concepts

* The `CALMS` culture of DevOps:
  * `C`ulture: Shared responsibility and collaboration.
  * `A`utomation: Automate everything possible.
  * `L`ean: Eliminate waste and focus on value.
  * `M`easurement: Measure everything, from delivery time to error rates.
  * `S`haring: Sharing knowledge and tools.
* `CI/CD` (Continuous Integration/Deployment): The heart of DevOps.
  * `CI` (Continuous Integration): Automatically building and testing code with every change.
  * `CD` (Continuous Delivery): Automatically preparing a deployable release after CI succeeds.
  * `CD` (Continuous Deployment): Automatically deploying this release to the production environment.
* `Infrastructure as Code (IaC)`: Managing infrastructure through version-controllable code files, instead of manual setup.
* `Configuration Management`: Ensuring that server and software configurations are consistent and managed via code (using tools like Ansible).
* `Monitoring vs. Observability`:
  * `Monitoring`: Collecting predefined metrics ("known unknowns").
  * `Observability`: The ability to ask arbitrary questions about your system's state without needing to pre-define metrics ("unknown unknowns"). It includes Logs, Metrics, and Traces.

## 5. Expanded Tools & Technologies

* Version Control: Git, GitHub, GitLab.
* CI/CD Tools: Jenkins, GitHub Actions, GitLab CI.
* Infrastructure as Code (IaC): Terraform, AWS CloudFormation.
* Configuration Management: Ansible, Puppet.
* Containers: Docker.
* Container Orchestration: Kubernetes.
* Monitoring: Prometheus, Grafana.
* Logging: ELK Stack (Elasticsearch, Logstash, Kibana).
* Scripting: Bash, Python.

## 6. In-Depth Workflow

Project: A developer has finished the "Login with Google" feature and created a Pull Request (PR).

 1. CI Trigger on PR: The DevOps engineer has set up a pipeline in GitHub Actions that runs automatically on every new PR. This pipeline runs unit and integration tests. The PR cannot be merged if the tests fail.
 2. CD Trigger on Merge: After the PR is reviewed and merged into the `main` branch, another, more comprehensive pipeline runs:
     * Build: The pipeline pulls the latest code and builds Docker images for the Frontend and Backend services.
     * Push: The new images are pushed to a container registry (like Amazon ECR).
     * Deploy to Staging: The pipeline uses a tool like Argo CD to update Kubernetes in the "Staging" environment to use the new image.
     * Run E2E Tests: Comprehensive tests are run on the Staging environment to ensure the entire application works correctly.
 3. Manual Promotion to Production: After a successful deployment to Staging, a team member clicks a "manual approval" button in the pipeline to promote the release to production.
 4. Deploy to Production: The pipeline now performs the same deployment process on the production Kubernetes cluster. It might use a strategy like Blue-Green Deployment, where the new version is deployed alongside the old one, and traffic is switched over only after confirming the new version is healthy.
 5. Monitoring: The DevOps engineer monitors Grafana dashboards. They have alerts configured in Prometheus that will fire if the error rate increases or response times slow down after the deployment. If that happens, they can quickly trigger a rollback to the previous stable version.

## 7. Common Job Roles

* DevOps Engineer
* Platform Engineer
* Build/Release Engineer
* Automation Engineer
* Site Reliability Engineer (SRE)

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Ansible`** | A configuration management and automation tool that does not require installing agents on target servers. |
| **`Argo CD`** | A tool that implements the `GitOps` principle for continuous deployment on `Kubernetes`. |
| **`Blue-Green Deployment`** | A deployment strategy where two versions (old and new) of the application are run, and traffic is switched between them. |
| **`Canary Deployment`** | A deployment strategy where a new feature is released to a small percentage of users first. |
| **`Configuration Management`** | The process of maintaining system and software configurations in a known, consistent state. |
| **`GitOps`** | A way of managing infrastructure and deployments where `Git` is the single source of truth. |
| **`Idempotency`** | The property of an operation that can be repeated multiple times without changing the result after the first run. |
| **`Jenkins`** | A very popular open-source automation server for building CI/CD pipelines. |
| **`Observability`** | The ability to understand the internal state of a system from its external data (Logs, Metrics, Traces). |
| **`Pipeline as Code`** | The practice of defining a CI/CD pipeline in a code file (like a `Jenkinsfile` or `github-actions.yml`). |
| **`SRE`** | Site Reliability Engineering, a discipline that applies software engineering principles to infrastructure and operations problems. |
| **`Terraform`** | The most popular tool for Infrastructure as Code (IaC). |

</details>

[⬆️ Back to Table of Contents](README.md)

