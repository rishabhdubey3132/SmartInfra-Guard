# SmartInfra Guard

**SmartInfra Guard** is an automated infrastructure monitoring and incident response system. It streams server logs in real time, uses a machine learning model to detect critical issues, and triggers remediation actions automatically. The system also tracks infrastructure metrics and presents them through live dashboards.

---

## Features

- Real-time log streaming from cloud servers
- Machine learning-based anomaly detection
- Automatic issue remediation (e.g., restart services, scale servers)
- Infrastructure metrics collection and visualization
- Modular design with separate components for prediction, monitoring, and automation

---

## Tech Stack

| Component       | Technology             | Role                                |
|----------------|------------------------|-------------------------------------|
| Log Streaming   | Apache Kafka           | Collects and streams server logs    |
| Prediction      | Python + ML            | Detects anomalies and potential failures |
| Auto-Fix Engine | Jenkins + Ansible      | Executes automated remediation      |
| Monitoring      | Prometheus + Grafana   | Tracks system metrics and alerts    |
| Infrastructure  | AWS + Terraform        | Infrastructure provisioning         |
| CI/CD           | GitHub Actions         | Builds, tests, and deploys code     |

---

## Architecture Overview

1. Logs are streamed from cloud servers using Kafka.
2. A Python service receives the logs and passes them to an ML model.
3. The model checks for failure indicators (e.g., high CPU, memory overload).
4. If a risk is detected, Jenkins triggers Ansible scripts to fix the issue.
5. Prometheus collects system metrics, which are visualized in Grafana dashboards.

