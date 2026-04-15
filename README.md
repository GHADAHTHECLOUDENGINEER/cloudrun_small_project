🚀 Google Cloud Run Deployment Project
📝 Project Overview
This project demonstrates the end-to-end process of containerizing a web application using Docker and deploying it to Google Cloud Platform (GCP) using Cloud Run. This was completed as part of my final bootcamp technical requirements.
🛠️ Tech Stack
Docker Desktop: For container management and image pulling.
Google Cloud SDK (gcloud): For CLI interaction with GCP.
Google Artifact Registry: As a private Docker host.
Google Cloud Run: For serverless container execution.
💻 Terminal Workflow & Commands
Here is the step-by-step technical process I followed:
1. Preparing the Image
I pulled the official Nginx image to use as my web application base:
docker pull nginx
2. GCP Authentication
gcloud auth login
gcloud auth configure-docker
3. Tagging the Image
I prepared the image for the Google Registry by tagging it with my Project ID:
docker tag nginx gcr.io/your-project-id/my-app-linkin
4. Pushing to Cloud Registry
I uploaded the container image from my local machine to the cloud:
docker push gcr.io/your-project-id/my-app-linkin
5. Deployment on Cloud Run
Finally, I deployed the service through the GCP Console with the following configurations:
Authentication: Enabled "Allow unauthenticated invocations" for public access.
Region: Selected the closest region for low latency.
🎯 Key Learning Outcomes
Understanding the difference between Docker Images and Containers.
Managing Cloud Artifacts and Repositories.
Configuring Public IAM policies for Serverless deployments.
