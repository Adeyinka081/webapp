# WebApp Deployment Project

A simple **Node.js web application** deployed using **Docker**, hosted on an **AWS EC2 instance**, and fully automated with **GitHub Actions CI/CD**.

---

## 🚀 Features

- Node.js + Express backend
- Dockerized for consistent deployments
- Hosted on AWS EC2
- Fully automated CI/CD pipeline:
  - Build Docker image
  - Push to Docker Hub
  - Deploy automatically to EC2

---

## 💻 Technologies Used

- **Node.js & Express** – backend framework
- **Docker** – containerization
- **Docker Hub** – image registry
- **AWS EC2** – cloud VM deployment
- **GitHub Actions** – CI/CD automation
- **SSH** – remote deployment

---

## 📦 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/webapp.git
cd webapp
2. Run locally
Install dependencies:

npm install
Start the app:

node index.js
Open in your browser:

http://localhost:3000
3. Build and run with Docker
Build Docker image:

docker build -t webapp:latest .
Run container:

docker run -p 3000:3000 webapp:latest
4. Access the deployed app
After pushing to GitHub, the CI/CD pipeline will deploy automatically to your EC2 instance.

Open the live app:

http://YOUR_EC2_PUBLIC_IP
⚙️ CI/CD Pipeline
Triggered on every push to main

Steps:

Checkout code

Build Docker image

Push image to Docker Hub

SSH into EC2 and deploy

GitHub Actions workflow file: .github/workflows/deploy.yml

🔐 Environment Setup
GitHub Secrets required:

DOCKER_USERNAME – Docker Hub username

DOCKER_PASSWORD – Docker Hub password

VM_HOST – EC2 public IP

VM_USER – EC2 username (usually ubuntu)

VM_SSH_KEY – Private key content (.pem file)

📈 Future Improvements
Add Nginx reverse proxy for production

Use Docker Compose for multi-container apps

Scale with Kubernetes / EKS

Add monitoring & logging (Prometheus, Grafana)