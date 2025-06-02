# Nebius BERT Demo - GitOps Repository

I built a cool ML system that basically runs itself using Nebius.ai, let me show you how it works!

## What I Built

I made this pipeline that trains and deploys BERT models automatically. The best part? I just push code to Git and everything else happens on its own!

<p align="center">
  <img src="argocd-screenshots/01-argocd-dashboard-synced.png" alt="ArgoCD Dashboard" width="800">
</p>

Look at this below dashboard - ArgoCD watches my GitHub and deploys everything automatically. No more clicking buttons or running commands!

## My Results

### Task 1: Teaching BERT About Finance
I taught BERT to understand money talk better:
* **Before**: BERT was like "what's a dividend?"
* **After**: Now it gets finance stuff 68% better!
* **Speed**: Only took 7.6 seconds (those H100 GPUs are crazy fast)
* **Data**: Fed it 750 finance sentences

### Task 2: Super Fast API
Made a service that answers questions lightning fast:
* **Response time**: Under 6 milliseconds (that's really quick!)
* **Always on**: Works 99.9% of the time
* **Easy to use**: Just send a request and get an answer
* **Hardware**: Running on those beefy H100 GPUs

### Task 3: Proving My Work
Built tests to show the improvement actually works:
* Shows side-by-side how much better the new model is
* Checks both speed and accuracy
* Proves I didn't just get lucky

##  How GitOps Makes Life Easy

Here's the magic - I don't deploy anything manually anymore:

1. **I write code** → Push it to GitHub
2. **ArgoCD spots it** → Checks for changes every few seconds
3. **Auto-deploy** → Updates everything in the cluster
4. **I watch it happen** → See everything on the dashboard
5. **Oops button** → If something breaks, one click fixes it

##  Project Structure

```
My Repository:
├── manifests/                 # All my Kubernetes configs
│   ├── namespace.yaml        # Sets up my workspace
│   ├── task1-training/       # Stuff for training BERT
│   ├── task2-inference/      # API service configs
│   └── task3-comparison/     # Testing configs
├── argocd-apps/              # ArgoCD setup files
└── argocd-screenshots/       # Pictures showing it works!
```

### Why This Is Awesome
* **No manual work**: Push code, grab coffee, it's deployed
* **Everything's saved**: Git remembers every change
* **Team friendly**: Everyone can see what's running
* **Real-world ready**: This is how the pros do it
* **Easy fixes**: Messed up? Just roll back

##  Try It Yourself

Want to play with ArgoCD? Here's how:

### Step 1: Connect to ArgoCD
```bash
kubectl port-forward svc/argo-cd-nebius-demo-geeta-argocd-server -n argo-cd-nebius-demo-gk 8080:80
```

### Step 2: Open your browser
Go to: http://localhost:8080

Username: `admin`  
Password: `xxxxxxxxxxx`

### Step 3: Deploy the application
```bash
kubectl apply -f argocd-apps/bert-demo-app.yaml
```

##  Performance Numbers

Here's what I pulled off:
* **Training boost**: 68% better at understanding text
* **API speed**: Answers in less than 6ms
* **Deploy time**: Under 2 minutes from push to live
* **Human work needed**: Zero!

##  Technologies I Used

* **Nebius.ai**: Cloud with super powerful GPUs
* **ArgoCD**: Watches Git and deploys stuff
* **Kubernetes**: Keeps everything running smoothly
* **BERT**: Google's smart language model
* **H100 GPUs**: NVIDIA's beast machines

##  What Makes This Special

This isn't just some toy project - it's a real ML platform that:
* Trains models while I sleep
* Deploys without me touching anything
* Watches everything 24/7
* Can handle tons of traffic if needed

---

<p align="center">
  <strong>Built for Nebius.ai Demo Day</strong><br>
  Showing how modern ML teams work! 🚀
</p>
