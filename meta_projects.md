## This is a file explaining organization of my repos and projects as I build them.

I plan to migrate all my projects to GCP by Feb 2023. As of now I still have bunch of projects(pure modeling) at Kaggle.

I started on GCP with 2 VMs on Vertex AI: one CPU only, another one with GPU. I have built several projects on each together with simple deployment within Vertex AI. Those two VMs have the two respective repos. Each repo contaains multiple projects. Currently I suspect that was a mistake and will probably move to one repo - one project architecture.

I plan to build projects with fixed datsets in the following manner:
1. Use Vertex AI VMs to do modeling. Save model artifact into an artifact bucket.
2. Use Cloud Shell to build a deployment with Flask web-app. I think I have figured out how to deploy via Google App Engine. I will try repreating this approach for all projects. See sales_budget project for a template.
3. Verify that evth works and push the project to GH.
4. Clone that repo to Vertex AI VM and start it from there. Delete the project directory from Cloud Shell VM.

In this pipeline Cloud Shell seems like a redundant step. The problem is that I cannot figure out how to access web preview from within Vertex AI machine. Plus VSCode editor in Cloud Shell is nicer than Vertex Ai alternative.

Streaming datasets projects are likely to be much more complex. Probably I will have to build full-blown data pipelines with Pub/Sub, BQ and maybe feature Store.
To do deployment I will probably need Cloud Run or Cloud Functions. Plus I will have to set up monitoring and reporting somehow.


Deploying projects following this template seems straightforward enough. I need not use Cloud Shell CLI. 'lynx <url> -dump' is probably good enough to test webapp locally. Editing html files and main.py to do what i want seem pretty simple.
  
 
  
  
Next steps in this pipeline:
- add unit tests
  
  
  

