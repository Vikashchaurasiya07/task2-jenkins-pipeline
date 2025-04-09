# Task 2: Jenkins CI/CD Pipeline with Docker 🐳

## 📌 Overview

This project demonstrates a fully automated **CI/CD pipeline using Jenkins** to build and deploy a Node.js ToDo application using Docker.

> 🚀 It is part of my DevOps Internship (Task 2) submission. 

---

## ⚙️ Tech Stack

- **Node.js**
- **Docker**
- **Jenkins**
- **GitHub**
- **Jenkins Pipelines (Declarative)**

---

##✅ Successful Pipeline Screenshot
![Screenshot (20)](https://github.com/user-attachments/assets/260e776b-3d34-4154-8def-d76106c24b59)
![Screenshot (19)](https://github.com/user-attachments/assets/ed68c65d-c8fa-4c61-9799-2ccb5cb8aff6)
![Screenshot (18)](https://github.com/user-attachments/assets/eb0d1060-63e6-4df0-8c2f-5a4e85758681)







---

## 🧪 Features

- Installs Node.js dependencies using `npm`
- Runs basic unit test placeholder
- Builds a Docker image for the app
- Designed to optionally deploy the container
- Fully integrated with Jenkins Declarative Pipeline

---

## 🔄 CI/CD Pipeline Stages

1. **Build Application**  
   → Installs all required dependencies

2. **Run Unit Tests**  
   → Placeholder stage for unit testing

3. **Build Docker Image**  
   → Creates a Docker image `nodejs-demo-app`

4. **Deploy (Optional)**  
   → Placeholder for future deployment steps

---

## 🐳 Docker Commands

### ✅ Build Image Locally (Manual)
```bash
docker build -t nodejs-demo-app .
docker run -d -p 3000:3000 --name todo-app nodejs-demo-app

