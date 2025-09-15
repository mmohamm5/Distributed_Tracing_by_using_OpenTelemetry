# 🎓 Thesis Project: Optimizing Distributed Tracing and Telemetry in Microservices Using OpenTelemetry

## 📘 Project Overview
This repository complements the master’s thesis titled  
**“Optimizing Distributed Tracing and Telemetry in Microservices Using OpenTelemetry”**,  
submitted by *Md Nur Mohammad* to **TH Köln – University of Applied Sciences** in **August 2025**.  

The project focuses on designing a Kubernetes-based observability stack using the OpenTelemetry Demo Application to evaluate the effectiveness of end-to-end tracing, metrics, and logging in a microservices environment.

---

## 🎯 Motivation
Microservices offer great flexibility but introduce operational complexity. Traditional monitoring tools often fail to correlate logs, metrics, and traces, resulting in:

- Delayed fault detection
- Increased MTTR (Mean Time to Resolution)
- Fragmented visibility across services

This thesis aims to address these challenges by leveraging **OpenTelemetry**, which provides:

- ✅ Vendor-neutral, scalable observability tooling  
- ✅ Improved traceability across polyglot microservices  
- ✅ Real-time performance and reliability insights  
- ✅ DevOps-compatible monitoring pipelines  

OpenTelemetry integrates seamlessly with tools like **Grafana**, **Prometheus**, and **Jaeger**.

---

## 🧰 Tech Stack

| Component      | Role                                 |
|----------------|--------------------------------------|
| OpenTelemetry  | Collection of traces, metrics, logs  |
| Jaeger         | Distributed tracing backend          |
| Prometheus     | Metrics scraping and alerting        |
| Grafana        | Unified dashboard visualizations     |
| Locust         | Load generator                       |
| Helm           | Kubernetes package manager           |
| Kubernetes     | Container orchestration platform     |

---

## 🚀 Quick Start – Kubernetes Deployment

### Prerequisites
- Helm 3
- Kubernetes cluster (Minikube, KIND, or cloud-based)
- kubectl CLI

### Deployment Steps

```bash
# 1. Clone the repository
git clone https://github.com/mmohamm5/Distributed_Tracing_by_using_OpenTelemetry.git

# 2. Navigate to the Helm chart directory
cd Distributed_Tracing_by_using_OpenTelemetry/helm/helm-chart/opentelemetry-demo

# 3. Install the Helm chart
helm install otel-demo . -n otel-demo --create-namespace

# 4. Alternatively, deploy using kubectl
kubectl create --namespace otel-demo -f https://github.com/mmohamm5/Distributed_Tracing_by_using_OpenTelemetry/blob/master/kubernetes/opentelemetry-demo.yaml
# or
cd Distributed_Tracing_by_using_OpenTelemetry/kubernetes
kubectl create --namespace otel-demo -f opentelemetry-demo.yaml

```

## 🔗 Accessing Services via Port Forwarding

After setting up the `frontend-proxy` port-forward, you can access the following interfaces locally:

- 🛒 **Web Store**: [http://localhost:8080/](http://localhost:8080/)
- 📊 **Grafana Dashboard**: [http://localhost:8080/grafana/](http://localhost:8080/grafana/)
- ⚙️ **Load Generator UI**: [http://localhost:8080/loadgen/](http://localhost:8080/loadgen/)
- 🔍 **Jaeger Tracing UI**: [http://localhost:8080/jaeger/ui/](http://localhost:8080/jaeger/ui/)
- 🚩 **Flagd Configurator UI**: [http://localhost:8080/feature](http://localhost:8080/feature)

---

## 📎 Repository Appendix: Master's Thesis

This GitHub repository accompanies the Master's thesis:

**Title**: *Optimizing Distributed Tracing and Telemetry in Microservices Using OpenTelemetry*  
**Author**: Md Nur Mohammad  
**University**: TH Köln – University of Applied Sciences  
**Submitted**: September 2025  
**Degree**: Master of Science in Communication Systems and Networks.

📄  "The thesis is available upon request from the author or the university archive."

📘 This repository contains the complete implementation, deployment scripts, configuration files, and dashboards referenced in the thesis.
