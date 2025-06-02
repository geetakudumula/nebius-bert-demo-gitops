# Nebius BERT Demo - GitOps Repository

This repository demonstrates GitOps practices for ML workloads on Nebius.ai platform.

## Demo Components

### Task 1: Distributed Training
- BERT fine-tuning on financial domain data
- Achieved 68% loss reduction
- Uses Nebius Soperator for distributed training

### Task 2: Inference Service
- Kubernetes-native inference deployment
- Sub-6ms latency on H100 GPUs
- REST API for model predictions

### Task 3: Model Comparison
- Performance benchmarking framework
- Original vs fine-tuned model comparison

## GitOps with ArgoCD
- Automated deployment pipeline
- Version-controlled infrastructure
- Easy rollback and updates

## Results
- Training Loss: 4.65 → 1.44 (68% reduction)
- Inference Latency: <6ms on H100
- Infrastructure: Fully automated with ArgoCD
