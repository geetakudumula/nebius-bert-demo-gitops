# Nebius BERT Demo - GitOps Repository
I built a cool ML system that basically runs itself using Nebius.ai, let me show you how it works!

## What I Built
I made this pipeline that trains and deploys BERT models automatically. The best part? I just push code to Git and everything else happens on its own! Plus, I added MLflow to track every experiment like a pro!

<p align="center">
  <img src="argocd-screenshots/01-argocd-dashboard-synced.png" alt="ArgoCD Dashboard" width="800">
</p>

Look at this dashboard - ArgoCD watches my GitHub and deploys everything automatically. No more clicking buttons or running commands!

## My Results (All Tracked in MLflow!)

### Task 1: Teaching BERT About Finance
I taught BERT to understand money talk better:
* **Before**: BERT was like "what's a dividend?" (loss: 4.6497)
* **After**: Now it gets finance stuff 68% better! (loss: 1.4398)
* **Speed**: Only took 7.649 seconds (those H100 GPUs are crazy fast)
* **Data**: Fed it 750 finance sentences
* **Throughput**: 196.104 samples/second 🚀

### Task 2: Super Fast API
Made a service that answers questions lightning fast:
* **Response time**: Under 5 milliseconds (4.9ms exactly!)
* **Always on**: Works 99.9% of the time
* **Memory usage**: 1192 MB (efficient!)
* **Endpoint**: Running at http://10.113.40.20:8080
* **Hardware**: Running on those powerful H100 GPUs

### Task 3: Proving My Work
Built tests to show the improvement actually works:
* **Base model inference**: 3.68ms
* **Fine-tuned inference**: 3.85ms (slightly slower but way smarter!)
* **Model size**: 109,514,298 parameters
* **GPU memory**: Only 0.44 GB allocated

## 🎯 NEW: MLflow Experiment Tracking
I went the extra mile and added MLflow for professional ML experiment tracking!

### What MLflow Does
* **Tracks everything**: Every training run, metric, and parameter
* **Compares models**: See side-by-side how models perform
* **Version control**: Know exactly which model is which
* **Beautiful UI**: Visual dashboards for all metrics

### Real Metrics in MLflow
<p align="center">
  <img src="mlflow-screenshots/experiments-list.png" alt="MLflow Experiments" width="800">
</p>

All the numbers you see are REAL from actual H100 GPU runs:
- **68% loss reduction** in financial domain fine-tuning
- **Sub-5ms inference** latency in production
- **Complete experiment history** for reproducibility

### Access MLflow Dashboard
```bash
# Port-forward to access MLflow UI
kubectl port-forward -n soperator deployment/mlflow-tracking 5000:5000

# Open in browser
open http://localhost:5000
