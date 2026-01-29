# 📊 Prometheus – Observability Fundamentals
**1️⃣ What is Observability?**

Observability is the ability to understand and measure the internal state of a system by analyzing the data it generates.
- It answers questions like:
- What is happening inside the system?
- Why did this issue occur?
- How can we prevent it in the future?

****2️⃣ How Observability Helps****

Observability enables teams to handle unexpected and complex scenarios by:
- Providing deep insight into the internal workings of systems and applications
- Speeding up troubleshooting and root cause analysis
- Detecting hard-to-catch and intermittent problems
- Monitoring application and infrastructure performance
- Improving collaboration across DevOps, SRE, and development teams

****3️⃣ Troubleshooting with Prometheus****

When troubleshooting, knowing what is wrong is not enough.
We also need to understand:
- Why the application entered a specific state
- Which component caused the issue
- How to prevent it from happening again

Common questions answered using observability:
- Why are error rates increasing?
- Why is application latency high?
- Why are services timing out?
👉 Observability provides the flexibility to analyze unpredictable events, which traditional monitoring alone cannot handle.

****4️⃣ Pillars of Observability****

Observability is achieved using three core pillars:
- Logs
- Metrics
- Traces

****5️⃣ Logging****

Logs are records of events that have occurred in a system and provide detailed information about specific events.
Log Components:
- Timestamp – When the event occurred
- Message – Information about the event
- Logs from multiple services and processes are often:
- Interwoven
- Distributed across multiple systems
- Difficult to correlate without observability tools
  
****6️⃣ Traces****

Traces help track a request as it travels through multiple systems and services.
They help answer:
- How requests flow through microservices
- Where latency is introduced
- Which service is failing

Trace Concepts:
Each request has a Trace ID
- A trace is composed of multiple Spans
- Each Span Tracks:
  - Start time
  - Duration
  - Parent ID (relationship to other spans)

****7️⃣ Metrics****

Metrics represent the state of a system using numerical values collected over time.
Examples:
- CPU load
- Number of open files
- HTTP response time
- Error count

Metrics can be:
- Aggregated
- Visualized
- Analyzed to identify trends and anomalies

****8️⃣ Metric Structure****

Each metric contains four key components:
- Metric Name
- Value – current or most recent value
- Timestamp
- Dimensions (Labels) – additional context

Example Metric:
node_filesystem_avail_bytes{fstype="vfat", mountpoint="/home"} 5000 12/01 04:30 AM
<pre>
|Metric Name                 | 	Dimensions	                   |  |Value | Timestamp|
|node_filesystem_avail_bytes | fstype="vfat", mountpoint="/home"|	|5000	 | 04:30 AM |
</pre>
# 🎯 Why Prometheus Fits Observability
- Strong metrics collection model
- Powerful querying with PromQL
- Native Kubernetes integration
- Ideal for performance monitoring and alerting
- Helps reduce MTTR in production environments
