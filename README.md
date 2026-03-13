# 🧠 AI Vision Analytics Platform

![Status](https://img.shields.io/badge/status-active-success.svg)
![Azure](https://img.shields.io/badge/Azure-AKS-blue.svg)
![ML](https://img.shields.io/badge/AI%2FML-Computer--Vision-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

**AI Vision Analytics** is a cloud-native, end-to-end platform for real-time visual intelligence. Designed to run on **Azure Kubernetes Service (AKS)**, it leverages SOTA object detection models to provide real-time telemetry and actionable insights from video streams.

---

## 🚀 Key Features

- **Real-time Inference**: Optimized YOLOv8/v10 serving via FastAPI and TensorRT.
- **Cloud-Native Scalability**: Auto-scaling inference pods on AKS with Azure Machine Learning integration.
- **MLOps Pipeline**: Automated model training, versioning, and deployment using GitHub Actions and Azure ML.
- **Visual Telemetry**: Real-time dashboard for object tracking, heatmaps, and anomaly detection.
- **High Reliability**: Integrated Prometheus/Grafana monitoring for model performance and system health.

## 🏗️ System Architecture

`mermaid
graph TD
    Stream[Video Stream / CCTV] -->|RTSP| Ingest[Ingestion Service]
    Ingest -->|Frames| Inference[AI Inference Engine - AKS]
    Inference -->|Detections| Analytics[Analytics Service]
    Analytics -->|Telemetry| DB[(CosmosDB / Redis)]
    Analytics -->|Visuals| WebUI[Visual Dashboard]
    MLOps[GitHub Actions] -->|Deploy| Inference
`

## 🛠️ Tech Stack

- **AI/ML**: Python, PyTorch, OpenCV, ONNX, Ultralytics.
- **Cloud**: Microsoft Azure (AKS, ACR, Azure ML, CosmosDB).
- **DevOps**: Docker, Kubernetes, Terraform, GitHub Actions.
- **Backend**: FastAPI, Go (for stream processing).

## 📂 Project Structure

\\\
ai-vision-analytics/
├── src/
│   ├── engine/              # Core AI inference logic
│   ├── api/                 # FastAPI service for detection results
│   └── utils/               # Image processing & telemetry helpers
├── deployment/
│   ├── k8s/                 # Kubernetes manifests (AKS)
│   └── terraform/           # IaC for Azure Infrastructure
├── Dockerfile               # Container definition
├── requirements.txt         # Dependencies
└── README.md
\\\

## 🧪 Quick Start

1. **Clone the repository**
   \\\ash
   git clone https://github.com/snapple-w/ai-vision-analytics.git
   cd ai-vision-analytics
   \\\

2. **Run Locally (Docker)**
   \\\ash
   docker build -t ai-vision .
   docker run -p 8000:8000 ai-vision
   \\\

## 👨‍💻 Author

**Hitesh Malhotra**
*Senior Software Engineer | Cloud Native & AI Specialist*
[LinkedIn](https://www.linkedin.com/in/hiteshmalhotra/)

---
*Empowering visual intelligence with cloud-native precision.*