# DevOps CI/CD Pipeline with Docker, Jenkins, and Nginx

## 📌 Project Overview

This project demonstrates a simple **DevOps CI/CD pipeline** using Docker containers, Jenkins automation, and an Nginx reverse proxy.

The system containerizes a Node.js application, deploys multiple instances of it, and routes traffic through Nginx while Jenkins manages automation tasks.

This setup showcases core DevOps practices such as:

* Containerization
* CI/CD automation
* Reverse proxy configuration
* Load balancing
* Infrastructure orchestration with Docker Compose

---

## 🏗 Architecture

Developer
⬇
GitHub Repository
⬇
Jenkins (CI/CD Pipeline)
⬇
Docker Image Build
⬇
Docker Containers (App Instances)
⬇
Nginx Reverse Proxy / Load Balancer
⬇
Users

---

## ⚙️ Tech Stack

* **Docker** – Containerization
* **Docker Compose** – Multi-container orchestration
* **Jenkins** – CI/CD automation
* **Nginx** – Reverse proxy and load balancing
* **Node.js (Express)** – Backend application
* **GitHub** – Source code management

---

## 🚀 Setup Instructions

### 1️⃣ Clone the repository

```
git clone https://github.com/YOUR_USERNAME/devops-ci-cd-project.git
cd devops-ci-cd-project
```

---

### 2️⃣ Install dependencies

```
cd app
npm install
cd ..
```

---

### 3️⃣ Start the containers

```
docker-compose up -d --build
```

This command starts the following services:

* Jenkins CI/CD server
* Nginx reverse proxy
* Two Node.js application containers

---

### 4️⃣ Verify running containers

```
docker ps
```

You should see containers for:

* Jenkins
* Nginx
* app1
* app2

---

## 🌐 Access the Services

Application:

```
http://SERVER-IP
```

Jenkins Dashboard:

```
http://SERVER-IP:8080
```

---

## 🔐 Jenkins Initial Setup

Retrieve the Jenkins unlock password:

```
docker exec devops-ci-cd-project_jenkins_1 cat /var/jenkins_home/secrets/initialAdminPassword
```

Then open the Jenkins dashboard and install the suggested plugins.

---

## 🔄 CI/CD Workflow

1. Developer pushes code to GitHub
2. Jenkins detects repository changes
3. Jenkins pipeline builds Docker images
4. Docker containers are deployed
5. Nginx routes traffic to running containers

---

## 👨‍💻 Author

Shruti Joshi
DevOps & Cloud Enthusiast
