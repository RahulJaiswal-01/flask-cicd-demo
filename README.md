# Flask CI/CD Pipeline

## Project Overview

This project demonstrates an automated CI/CD pipeline using:

- GitHub
- Jenkins
- Docker
- Linux

Whenever code is pushed to GitHub, Jenkins automatically:

1. Pulls latest code
2. Builds Docker image
3. Deploys container

## Technologies Used

- Python
- Flask
- Jenkins
- Docker
- Git
- GitHub
- Linux

## Project Structure

```
flask-app/
├── app.py
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
└── README.md
```
## Architecture Diagram

```
Developer
    │
    ▼
 GitHub
    │
    ▼
 Jenkins
    │
    ▼
 Docker Build
    │
    ▼
 Container Deployment

```

## Run Locally

```bash
docker build -t flask-app .
docker run -d -p 5000:5000 flask-app
```

## Jenkins Pipeline

Checkout SCM
↓
Build Docker Image
↓
Deploy Container

## Author

Rahul Jaiswal
