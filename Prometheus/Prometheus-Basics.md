# 🏗️ Prometheus Architecture

Prometheus follows a pull-based monitoring architecture designed for reliability, scalability, and cloud-native environments.

****🔁 High-Level Flow****
<pre>Targets / Exporters
        ↓
   Prometheus Server
        ↓
 Time-Series Database (TSDB)
        ↓
PromQL Query Engine
        ↓
Dashboards / Alerts
        ↓
   Alertmanager
</pre>  
# 🧩 Core Components
****1️⃣ Prometheus Server****

The Prometheus Server is the heart of the architecture.

Responsibilities:
- Scrapes metrics from configured targets
- Stores metrics as time-series data
- Evaluates recording rules and alert rules
- Serves data via PromQL

Main Parts:
- Retrieval (Scraping)
- TSDB (Time-Series Database)
- HTTP Server (Query API)

****2️⃣ Targets & Exporters****

Prometheus collects metrics by scraping HTTP endpoints exposed by targets.

Examples:
- Node Exporter – Linux system metrics
- cAdvisor – Container metrics
- Kube-State-Metrics – Kubernetes object states
- Application Exporters – Custom app metrics

Metrics endpoint:
```
http://<target>:<port>/metrics
```

****3️⃣ Service Discovery****

Prometheus dynamically discovers targets using service discovery mechanisms.

Supported Discovery:
- Kubernetes
- EC2
- Consul
- DNS
- Static configs
  
This enables monitoring in dynamic environments where IPs frequently change.

****4️⃣ Time-Series Database (TSDB)****

Prometheus stores data locally in a highly optimized TSDB.

Characteristics:
- Time-stamped data
- Label-based indexing
- Efficient compression
- Retention-based storage

⚠️ Prometheus is not a long-term storage solution by default.

****5️⃣ PromQL (Query Engine)****

PromQL is used to:
- Query metrics
- Aggregate data
- Perform calculations
- Build dashboards and alerts

Example:
- rate(http_requests_total[5m])

****6️⃣ Alertmanager****

Alertmanager handles alerts sent by Prometheus.

Responsibilities:
- Deduplication
- Grouping
- Silencing

Routing alerts to:
- Email
- Slack
- PagerDuty
- Webhooks

****7️⃣ Visualization (Grafana)****

Grafana is commonly used with Prometheus to:
- Build dashboards
- Visualize trends
- Correlate metrics
- Support troubleshooting
- Prometheus acts as the data source.
  
****☸️ Prometheus in Kubernetes****

In Kubernetes environments:
- Prometheus runs as a pod
- Uses Kubernetes service discovery
- Monitors nodes, pods, services, and workloads

Key Kubernetes exporters:
- kube-state-metrics
- cAdvisor
- Node Exporter

# ☁️ Prometheus in Cloud (AWS)

- Monitors EC2 instances via Node Exporter
- Discovers targets using EC2 service discovery
- Can integrate with CloudWatch exporters
- Often paired with long-term storage (Thanos/Cortex)

****🔐 Security Considerations****
- Secure /metrics endpoints
- Use TLS and authentication
- Restrict network access
- Protect Prometheus UI & API

# 🎯 Key Architectural Advantages
Pull-based model (better reliability)
Label-based metrics (high flexibility)
Strong Kubernetes integration
Simple yet powerful design

# 🧠 Summary

Prometheus scrapes metrics, stores time-series data, and enables querying
Alertmanager handles notifications
Grafana provides visualization

Architecture is ideal for cloud-native & microservices
