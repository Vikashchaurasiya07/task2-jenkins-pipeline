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
![Screenshot (16)](https://github.com/user-attachments/assets/3094b87d-ba57-474e-a51c-b9f3e2bddab1)
![Screenshot (15)](https://github.com/user-attachments/assets/9b27110d-ea9a-471d-babc-792dc2f53022)
![Screenshot (17)](https://github.com/user-attachments/assets/97aebda6-aa25-4119-8075-dbc7d4e05166)


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

