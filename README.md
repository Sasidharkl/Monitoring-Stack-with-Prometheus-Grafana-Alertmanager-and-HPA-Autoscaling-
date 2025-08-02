# 📈 Monitoring Stack with Prometheus, Grafana, Alertmanager, and Kubernetes Autoscaling

This project sets up a full monitoring and alerting stack using **Prometheus**, **Grafana**, and **Alertmanager** on **Kubernetes**, with support for **Horizontal Pod Autoscaling (HPA)** based on CPU utilization.

---

## 🧩 Stack Components

| Component     | Description                                           |
|---------------|-------------------------------------------------------|
| Prometheus    | Collects and stores metrics from nodes and pods       |
| Grafana       | Visualizes metrics from Prometheus                    |
| Alertmanager  | Sends alerts via email/Slack/Webhooks                 |
| HPA           | Automatically scales pods based on CPU usage          |
| Kube-State-Metrics | Exposes detailed pod/node metrics to Prometheus |

---

📊 Grafana Dashboard Setup
Navigate to Grafana UI

Add Prometheus as a data source (http://prometheus:9090)

Import dashboards manually or create custom dashboards

🔔 Alertmanager Configuration
Edit alertmanager/config-map.yaml to add:

Email configs

Slack Webhook configs

Custom routing

⚙️ Horizontal Pod Autoscaler (HPA)
Uses Kubernetes’ native HPA object:

Automatically increases/decreases pod replicas of cpu-stress-app

Triggered when CPU usage exceeds 50%

🧰 Prerequisites
Kubernetes cluster (Minikube, k3s, EKS, etc.)

kubectl installed

Optionally: Helm, Ingress Controller

📌 TODOs (optional improvements)
Use Helm charts for better configuration

Add Node Exporter for full system metrics

Integrate Slack/Discord Webhook for real-time alerts

Add dashboards via Grafana provisioning


