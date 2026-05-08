<div align="center">

# Avnish R. Singh

**AI Engineer · MLOps Engineer**

Production ML/GenAI systems · Multi-agent LLM applications · GNN-based security research · 4 peer-reviewed publications

[![LinkedIn](https://img.shields.io/badge/LinkedIn-avnishsingh17-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/avnishsingh17)
[![Email](https://img.shields.io/badge/Email-avnish1708%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:avnish1708@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-4285F4?style=flat-square&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1DWhfk8VESHzQjVofqHUUy8jluDHW00ax/view)
[![X](https://img.shields.io/badge/X-avnish__s17-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/avnish_s17)

</div>

---

## About

Building production-oriented GenAI and MLOps systems for **AI Engineer** and **MLOps Engineer** roles: RAG platforms, multi-agent LLM workflows, cloud-native inference services, CI/CD pipelines, and ML monitoring. Currently Junior Research Fellow at NIT Raipur (Dept. of IT), working on GNN-based threat detection using large-scale DARPA provenance graphs.

My strongest work combines applied ML research with deployment-focused engineering: 99%+ F1 scores on graph-based security datasets, federated learning across heterogeneous clients, GCP infrastructure with Terraform and GKE, and 4 peer-reviewed publications.

---

## Skills

| Category | Technologies / Areas |
|---|---|
| **Languages** | Python, SQL, Bash |
| **ML and Deep Learning** | PyTorch, PyTorch Geometric, Scikit-learn, NumPy, Pandas |
| **Graph ML and Research ML** | Graph neural networks, node embeddings, provenance graphs, federated learning |
| **LLM and Agentic AI** | LangChain, LangGraph, AutoGen, FAISS, RAG |
| **MLOps and Deployment** | Docker, Kubernetes, Redis, model serving, drift monitoring |
| **Cloud and Infrastructure** | GCP (GKE, Artifact Registry, Workload Identity), AWS (EC2, ECR), Terraform |
| **Security Research Lab** | GNS3, Kali Linux, Ubuntu, SPADE, Neo4j, attack simulation, provenance data collection |
| **APIs and UI** | FastAPI, Flask, Streamlit |
| **CI/CD and Monitoring** | GitHub Actions, Prometheus, Grafana |

---

## Projects

### Document Portal: Enterprise RAG Platform

[![GitHub](https://img.shields.io/badge/GitHub-document__portal-181717?style=flat-square&logo=github)](https://github.com/avnishs17/document_portal)
&nbsp;`FastAPI` `LangChain` `FAISS` `Gemini` `Groq` `Docker` `GKE` `Terraform` `GitHub Actions`

- Built multi-document chat, semantic search, and document comparison using session-scoped FAISS indexes to isolate concurrent users and avoid shared-state conflicts
- Full GCP stack provisioned from zero with Terraform: custom VPC, GKE cluster with autoscaling node pools, Artifact Registry, Workload Identity Federation, static external IP
- End-to-end CI/CD on GitHub Actions: Terraform plan/apply, Docker build and push to Artifact Registry, rolling Kubernetes deployment triggered on every push to master

---

### Data Insight AutoGen: Multi-Agent Analysis Platform

[![GitHub](https://img.shields.io/badge/GitHub-data__insight__autogen-181717?style=flat-square&logo=github)](https://github.com/avnishs17/data_insight_autogen)
&nbsp;`Streamlit` `AutoGen` `Gemini` `Docker` `Python`

- Two-agent pipeline: DataAnalyzer generates Python analysis code from natural language queries; CodeExecutor runs it in an isolated Docker container with automatic error recovery and on-the-fly dependency installation
- Multi-turn conversation state persists across Streamlit sessions; visualizations generated inside Docker surface automatically to the UI

---

### AI Travel Planner: Multi-Agent Planning System

[![GitHub](https://img.shields.io/badge/GitHub-Trip__planner__AI2-181717?style=flat-square&logo=github)](https://github.com/avnishs17/Trip_planner_AI2)
&nbsp;`LangGraph` `LangChain` `FastAPI` `Flask` `Groq` `Tavily` `Docker` `GKE` `GitHub Actions`

- LangGraph multi-agent system with four tool-equipped agents covering weather forecasting, place search (Tavily), currency conversion, and expense calculation
- Dual-service (FastAPI backend, Flask frontend) containerized deployment on GKE with HPA autoscaling (2-10 replicas) and Kubernetes Secrets for API key management

---

### MLOps Pipeline with Monitoring

[![GitHub](https://img.shields.io/badge/GitHub-user__survival__prediction-181717?style=flat-square&logo=github)](https://github.com/avnishs17/user_survival_prediction)
&nbsp;`GCP Cloud Storage` `PostgreSQL` `Redis` `Scikit-learn` `Prometheus` `Grafana` `Docker`

- Pipeline orchestrates ingestion from GCP Cloud Storage, feature engineering with SMOTE class balancing, Redis-backed feature store, and Random Forest training with RandomizedSearchCV
- Flask inference server instrumented with Prometheus for prediction volume tracking and KSDrift-based input drift detection, surfaced in Grafana dashboards
- Full monitoring stack containerized via Docker Compose; reproducible across local and cloud environments

---

## Research and Applied ML Work

### Junior Research Fellow, NIT Raipur (Jul 2024 - Present)

Applied graph ML and federated learning to cybersecurity datasets, with focus on APT detection, provenance graphs, heterogeneous clients, and edge inference feasibility.

**Provenance Data Collection Lab**

- Built a GNS3 cyber range with one public subnet and two private subnets, using Kali Linux attacker machines and Ubuntu victims instrumented with SPADE; stored provenance graphs in Neo4j and extracted session-level JSON graphs with Python
- Simulated normal workflows and kill-chain attacks including brute force, reverse shell, and VSFTPD backdoor; labeled malicious nodes using predefined Kali command timelines and victim-side activity traces

**APT Detection via GNNs on Provenance Graphs**

- Datasets include custom SPADE/GNS3 provenance graphs, DARPA E3 (CADETS, THEIA, TRACE), StreamSpot, Unicorn, and CICAPT-IIoT 2024
- Heterogeneous provenance graphs include process, file, and network activity with multiple edge types
- Self-supervised GNN masked autoencoder for representation learning; binary classifiers used for malicious node detection
- F1 score above 99% on evaluated DARPA E3 provenance datasets

**Federated Threat Detection**

- FedNODE workflow implemented with Flower (flwr) on EdgeIIoTSet using IID client splits
- Multi-class classification across 3, 5, 7, and 10 clients with fixed 10-round runs for each client configuration
- F1 >= 0.976 across tested client configurations

**Edge Inference Prototype**

- Proof-of-concept edge pipeline with pretrained encoder hosted on laptop and trained classifier hosted on Raspberry Pi 5
- Streaming module passes graph data through the encoder, sends node embeddings to Raspberry Pi 5, and runs classifier inference on-device
- Raspberry Pi 5 computes inference metrics and exports logs to Prometheus; Grafana dashboard runs on the laptop for visualization

---

## Publications

| Type | Title | Venue | Year |
|---|---|---|---|
| Journal | GCN-LSTM: A Hybrid Graph Convolutional Network Model for Schizophrenia Classification | *Biomedical Signal Processing and Control*, Elsevier **(Q1, 10+ citations)** | 2025 |
| Conference | Advanced Persistent Threats Detection Framework for Industrial-IoT System Using Graph-Based Autoencoder and Stacking-Based Ensemble Technique | *International Symposium on Artificial Intelligence*, Springer | 2025 |
| Conference | Fed-NODE: Federated Learning Based Threat Detection Framework for Edge-Based Industrial Internet of Things | *MIND 2025*, MNIT Jaipur | 2025 |
| Book Chapter | Foundations of Edge Intelligence | *Edge Intelligence and Analytics for Internet of Things*, CRC Press | 2025 |

[Full publication list](https://drive.google.com/file/d/1tE0we464Coj7r8zfQQY3Rup2JBGB4gYn/view?usp=sharing)

---

## Education

| Degree | Institution | Year | CGPA |
|---|---|---|---|
| M.Sc. Computational Science and Applications (Data Science) | Banaras Hindu University | 2024 | 8.3 / 10 |
| B.Sc. Computer Science | D.G. Ruparel College, University of Mumbai | 2022 | 8.75 / 10 |

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-avnishsingh17-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/avnishsingh17)
[![Email](https://img.shields.io/badge/Email-avnish1708%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:avnish1708@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-4285F4?style=flat-square&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1DWhfk8VESHzQjVofqHUUy8jluDHW00ax/view)
[![X](https://img.shields.io/badge/X-avnish__s17-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/avnish_s17)
