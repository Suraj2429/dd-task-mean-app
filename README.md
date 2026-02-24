# 🚀 DevOps Internship Assignment  
## MEAN Stack Application – Containerization, CI/CD & Cloud Deployment

👨‍💻 **Candidate:** Suraj Patil  
🌐 **Live Application URL:**  
http://43.205.140.151/

---

# 📌 Project Overview

This project demonstrates complete containerization and automated deployment of a full-stack **MEAN (MongoDB, Express, Angular, Node.js)** application.

The application has been:

- ✅ Containerized using Docker  
- ✅ Deployed on AWS EC2 (Ubuntu)  
- ✅ Configured using Docker Compose  
- ✅ Automated using GitHub Actions (CI/CD)  
- ✅ Exposed using Nginx Reverse Proxy on Port 80  

---

# 🏗️ Architecture Flow

Developer Push  
⬇  
GitHub Repository  
⬇  
GitHub Actions CI/CD  
⬇  
Docker Hub (Image Push)  
⬇  
AWS EC2 (Ubuntu VM)  
⬇  
Docker Compose Deployment  
⬇  
Nginx Reverse Proxy (Port 80)  
⬇  
Live Application  

---

# 🛠️ Technologies Used

- MongoDB  
- Express.js  
- Angular  
- Node.js  
- Docker  
- Docker Compose  
- GitHub Actions  
- AWS EC2 (Ubuntu)  
- Nginx  

---

# 📂 Repository Setup

- Created a new GitHub repository  
- Pushed frontend and backend source code  
- Added Dockerfiles for both services  
- Added `docker-compose.yml`  
- Configured GitHub Actions workflow  

---

# 🐳 Docker Configuration

## Backend
- Base Image: Node  
- Exposed Port: 8080  
- Production-ready build  
- Connected to MongoDB container  

## Frontend
- Multi-stage Docker build  
- Angular build stage  
- Nginx production stage  
- Exposed Port: 80  

---

# 🐳 Docker Images

### Backend Image
supra29/dd_task-backend:latest

### Frontend Image
supra29/dd_task-frontend:latest

Images are automatically built and pushed via CI/CD.

---

# ☁️ Cloud Infrastructure

- Cloud Provider: AWS  
- Region: ap-south-1 (Mumbai)  
- Instance Type: t3.micro  
- OS: Ubuntu  
- Security Group Ports:  
  - 22 (SSH)  
  - 80 (Application Access)  
  - 8080 (Backend internal)  

Infrastructure is preserved as requested.

---

# 🗄️ Database Setup

MongoDB is deployed using the official MongoDB Docker image.

Service Name: `mongodb`  
Port: `27017`  
Configured inside `docker-compose.yml`

---

# 🐳 Docker Compose Deployment

## Services

- frontend  
- backend  
- mongodb  


## Command Used on EC2

```bash
docker-compose up -d
          
