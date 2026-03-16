# 🚀 mlops-nlp-master1

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-2.8%2B-0194E2?logo=mlflow&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Airflow](https://img.shields.io/badge/Apache_Airflow-2.7%2B-017CEE?logo=apacheairflow&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗_Hugging_Face-Transformers-yellow)
![Status](https://img.shields.io/badge/Status-Complet%20✅-brightgreen)

**École IT — Master 1 — Unité 3 BigData — Semaine 11 — Module M1MLOP**

> Notebooks de cours et travaux pratiques du module **M1MLOP — MLOps et Natural Language Processing**.  
> Formation de **35 heures (5 jours)** couvrant le déploiement de modèles ML en production, l'orchestration de pipelines, le monitoring, et les techniques modernes de NLP avec les Transformers.

---

## 🗂️ Structure du projet

```
mlops-nlp-master1/
│
├── 📓 jour1/
│   └── jour1_mlops_fondements.ipynb
│       ├── TP 1.1 — MLflow Tracking (3 modèles, params, métriques, artefacts)
│       └── TP 1.2 — MLflow Registry (Staging → Production, rollback)
│
├── 📓 jour2/
│   └── jour2_pipelines_orchestration.ipynb
│       ├── TP 2.1 — DAG Airflow séquentiel (4 tasks)
│       ├── TP 2.2 — DAG parallèle (3 modèles simultanés)
│       ├── TP 2.3 — Tests pytest (unit + model + integration)
│       ├── TP 2.4 — API Flask + Dockerfile
│       └── TP 2.5 — Manifests Kubernetes (deployment, service, HPA)
│
├── 📓 jour3/
│   └── jour3_monitoring_gouvernance.ipynb
│       ├── TP 3.1 — Drift Detection KS test (3 niveaux)
│       ├── TP 3.2 — Métriques Prometheus + Dashboard
│       ├── TP 3.3 — A/B Testing Chi-Square
│       └── TP 3.4 — Fairness & Détection de biais
│
├── 📓 jour4/
│   └── jour4_nlp_transformers.ipynb
│       ├── TP 4.1 — Tokenisation + TF-IDF + Tokenizer HF
│       ├── TP 4.2 — Fine-tuning DistilBERT (Sentiment Analysis)
│       ├── TP 4.3 — NER (Named Entity Recognition)
│       └── TP 4.4 — API Flask NLP + Dockerfile
│
├── 📓 jour5/
│   └── jour5_integration_projet_final.ipynb
│       ├── Dataset : 200 tickets support (5 catégories)
│       ├── TP 5.1 — Pipeline Airflow NLP (5 tasks + MLflow)
│       ├── TP 5.2 — API FastAPI + Prometheus (4 endpoints)
│       ├── TP 5.3 — Batching & Caching (speedup comparison)
│       ├── TP 5.4 — Kubernetes HPA + Rolling Update
│       └── 🎯 Projet Final — Ticket Classifier System
│
├── 📋 requirements.txt
├── 📄 LICENSE
└── 📖 README.md
```

---

## 📅 Programme complet

| Jour | Thème | Outils principaux | TPs | Status |
|------|-------|-------------------|-----|--------|
| **Jour 1** | Fondements MLOps | MLflow, scikit-learn | Tracking, Registry, Rollback | ✅ Complet |
| **Jour 2** | Pipelines & Orchestration | Airflow, Docker, Kubernetes | DAGs, CI/CD, API, K8s | ✅ Complet |
| **Jour 3** | Monitoring & Gouvernance | Prometheus, SHAP, scipy | Drift, A/B Test, Fairness | ✅ Complet |
| **Jour 4** | NLP & Transformers | BERT, Hugging Face, spaCy | Fine-tuning, NER, QA | ✅ Complet |
| **Jour 5** | Intégration & Projet Final | FastAPI, Kubernetes HPA | Pipeline complet, Ticket Classifier | ✅ Complet |

---

## ⚡ Démarrage rapide

### 1. Cloner le dépôt
```bash
git clone https://github.com/Amadou-M/mlops-nlp-master1.git
cd mlops-nlp-master1
```

### 2. Créer un environnement virtuel
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate
```

### 3. Installer les dépendances
```bash
pip install -r requirements.txt
```

### 4. Lancer Jupyter
```bash
jupyter notebook
```

### 5. Lancer l'UI MLflow (Jour 1)
```bash
mlflow ui --backend-store-uri ./mlruns
# → http://localhost:5000
```

### 6. Lancer Airflow (Jour 2 & 5)
```bash
export AIRFLOW_HOME=~/airflow
airflow db init
airflow webserver --port 8080 &
airflow scheduler
# → http://localhost:8080
```

---

## 📦 Prérequis

| Outil | Version | Usage |
|-------|---------|-------|
| Python | 3.10+ | Langage principal |
| pip | récent | Gestionnaire de paquets |
| Git | récent | Versioning |
| Docker | récent | Conteneurisation (Jour 2, 4, 5) |
| kubectl | récent | Kubernetes (Jour 2, 5) |
| ~3 Go disque | — | Modèles NLP Hugging Face (Jour 4) |

---

## 🔧 Stack technique complète

| Catégorie | Outils |
|-----------|--------|
| **ML & MLOps** | `mlflow`, `scikit-learn`, `pandas`, `numpy` |
| **Orchestration** | `apache-airflow` |
| **NLP** | `transformers`, `torch`, `spacy`, `datasets` |
| **API** | `fastapi`, `uvicorn`, `flask`, `pydantic` |
| **Monitoring** | `prometheus-client`, `scipy` |
| **Conteneurisation** | `docker`, `kubernetes` |
| **Visualisation** | `matplotlib`, `seaborn` |
| **Tests** | `pytest` |

---

## 🎯 Projet Final — Ticket Classifier

> **Contexte** : Tu es ML Engineer dans une entreprise SaaS. Le support client reçoit 500+ tickets/jour. L'objectif est de les classifier automatiquement pour les router aux bonnes équipes.

### Catégories

| Catégorie | Équipe assignée |
|-----------|----------------|
| `BUG` | Dev Team |
| `FEATURE` | Product Team |
| `BILLING` | Finance Team |
| `ACCOUNT` | Support L1 |
| `PERFORMANCE` | Infra Team |

### Architecture complète

```
tickets.csv (200 exemples)
    │
    ▼
Airflow DAG (5 tasks)
extract → preprocess → train → validate → deploy
    │              └── MLflow tracking ──┘
    ▼
MLflow Registry (Staging → Production)
    │
    ▼
FastAPI (/predict, /batch_predict, /health, /info)
    ├── Prometheus metrics (Counter, Gauge, Histogram)
    └── LRU Cache (évite recalculs)
    │
    ▼
Kubernetes (3 replicas + HPA auto-scaling + Rolling Update)
```

### Livrables du projet

| Fichier | Description |
|---------|-------------|
| `data/raw/tickets.csv` | 200 tickets labelisés (5 catégories) |
| `models/ticket_classifier.pkl` | TF-IDF + LogisticRegression entraîné |
| `src/api.py` | API FastAPI complète avec Prometheus |
| `airflow/dags/ticket_classification_pipeline.py` | DAG Airflow 5 tasks |
| `kubernetes/deployment.yaml` | 3 replicas + rolling update |
| `kubernetes/service.yaml` | LoadBalancer |
| `kubernetes/hpa.yaml` | Auto-scaling CPU/RAM |
| `Dockerfile` | Conteneurisation production |
| `docker-compose.yml` | Environnement de dev complet |
| `tests/test_model.py` | Tests qualité + robustesse |
| `tests/test_pipeline.py` | Tests preprocessing + dataset |

### Critères d'évaluation

| Critère | Points |
|---------|--------|
| Modèle ML (Accuracy ≥ 80%, F1 ≥ 0.75) | 20 |
| Pipeline Airflow (4+ tasks, error handling) | 20 |
| API FastAPI (endpoints, validation) | 15 |
| Monitoring (Prometheus + logs) | 15 |
| Déploiement (Dockerfile + K8s) | 15 |
| Code Quality (tests + documentation) | 10 |
| Présentation | 5 |
| **Total** | **100** |

---

## 📸 Graphiques générés

| Notebook | Graphiques produits |
|----------|---------------------|
| Jour 1 | `iris_exploration.png`, `model_comparison.png`, `confusion_matrix.png` |
| Jour 2 | `dag_parallel_visualization.png` |
| Jour 3 | `drift_detection_visualization.png`, `monitoring_dashboard.png`, `explicabilite_shap.png`, `fairness_bias_detection.png` |
| Jour 4 | `embeddings_pca.png`, `nlp_drift_detection.png` |
| Jour 5 | `ticket_classifier_results.png`, `optimization_comparison.png` |

---

## 🚀 Commandes Docker

```bash
# Builder l'image du Ticket Classifier
docker build -t ticket-classifier:1.0 .

# Lancer en local
docker run -p 5000:5000 -p 8000:8000 ticket-classifier:1.0

# Lancer avec docker-compose (API + Prometheus + Grafana)
docker-compose up

# Tester l'API
curl -X POST http://localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"text": "Application crash quand je clique sur soumettre"}'
```

## ☸️ Commandes Kubernetes

```bash
# Déployer tout
kubectl apply -f kubernetes/

# Vérifier les pods et l'autoscaler
kubectl get pods
kubectl get hpa

# Voir les logs
kubectl logs deployment/ticket-classifier

# Scaler manuellement
kubectl scale deployment ticket-classifier --replicas=5

# Rolling update zero-downtime
kubectl set image deployment/ticket-classifier \
  ticket-api=ticket-classifier:2.0
kubectl rollout status deployment/ticket-classifier
```

---

## 🧪 Lancer les tests

```bash
# Tous les tests
pytest tests/ -v

# Avec rapport court
pytest tests/ -v --tb=short

# Un fichier spécifique
pytest tests/test_model.py -v
```

---

## 👤 Auteur

**Amadou MAIGA**  
Master 1 — École IT  
Année académique 2025-2026  
🔗 [GitHub](https://github.com/Amadou-M/mlops-nlp-master1)

---

## 📚 Ressources

| Ressource | Lien |
|-----------|------|
| MLflow Documentation | [mlflow.org](https://mlflow.org) |
| Apache Airflow | [airflow.apache.org](https://airflow.apache.org) |
| Hugging Face | [huggingface.co/docs](https://huggingface.co/docs) |
| FastAPI | [fastapi.tiangolo.com](https://fastapi.tiangolo.com) |
| Prometheus | [prometheus.io](https://prometheus.io) |
| Kubernetes | [kubernetes.io](https://kubernetes.io) |

---

## 📄 Licence

Ce projet est sous licence [MIT](LICENSE).  
Usage académique — École IT — Module M1MLOP.

---

*École IT — M1MLOP — MLOps & NLP — Année académique 2025-2026*
