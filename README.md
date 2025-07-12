# Jenkins CI/CD Learning Project

A comprehensive Jenkins CI/CD learning repository that demonstrates various deployment strategies and DevOps practices using a Flask web application. This project covers everything from basic Jenkins pipelines to advanced deployment patterns including Docker, Kubernetes, Lambda, and single-server deployments.

## 🏗️ Project Overview

This repository contains multiple Jenkins deployment scenarios, each building upon the previous one to demonstrate increasingly complex CI/CD patterns. The core application is a simple Flask-based task management web app that serves as the foundation for all deployment examples.

## 📁 Project Structure

```
jenkins-project/
├── jenkins-basics/          # Basic Jenkins pipeline setup
├── docker/                  # Docker containerization
├── single-server-deployment/ # Traditional server deployment
├── kubernetes/              # Kubernetes orchestration
├── lambda-deployment/       # AWS Lambda serverless deployment
└── 06-advanced-project/     # Advanced CI/CD with code quality and release management
```

## 🚀 Deployment Scenarios

### 1. Jenkins Basics (`jenkins-basics/`)
- **Purpose**: Introduction to Jenkins pipelines
- **Features**:
  - Basic CI pipeline with checkout, setup, and test stages
  - Python dependency management
  - Unit testing with pytest
- **Pipeline**: Basic declarative pipeline
- **Use Case**: Learning Jenkins fundamentals

### 2. Docker Deployment (`docker/`)
- **Purpose**: Containerization with Docker
- **Features**:
  - Docker image building and deployment
  - Container orchestration
  - Service configuration
- **Pipeline**: Docker build and deploy pipeline
- **Use Case**: Modern containerized applications

### 3. Single Server Deployment (`single-server-deployment/`)
- **Purpose**: Traditional server deployment
- **Features**:
  - Direct server deployment
  - SystemD service configuration (`flask.service`)
  - Manual deployment scripts
- **Pipeline**: Server-based deployment pipeline
- **Use Case**: Legacy application deployment

### 4. Kubernetes Deployment (`kubernetes/`)
- **Purpose**: Container orchestration with Kubernetes
- **Features**:
  - Kubernetes manifests (deployment.yaml, service.yaml)
  - Docker Hub integration
  - Automated K8s deployments
  - Acceptance testing with Node.js
- **Pipeline**: Complete K8s CI/CD pipeline
- **Use Case**: Scalable cloud-native applications

### 5. Lambda Deployment (`lambda-deployment/`)
- **Purpose**: Serverless deployment on AWS Lambda
- **Features**:
  - AWS SAM (Serverless Application Model)
  - Lambda function deployment
  - API Gateway integration
  - IAM policy configuration
- **Pipeline**: Serverless deployment pipeline
- **Use Case**: Event-driven, serverless applications

### 6. Advanced Project (`06-advanced-project/`)
- **Purpose**: Production-ready CI/CD with advanced features
- **Features**:
  - **Code Quality Pipeline** (`Jenkinsfile-Code-Quality`):
    - Static code analysis
    - Security scanning
    - Quality gates
  - **Release Pipeline** (`Jenkinsfile-Release`):
    - Git tag-based releases
    - Multi-environment deployments
    - Production release management
  - Poetry for dependency management
  - Comprehensive testing strategy
- **Pipeline**: Dual pipeline setup for quality and releases
- **Use Case**: Enterprise-grade CI/CD

## 🛠️ Core Application

The Flask application (`app.py`) is a simple task management system featuring:
- Add new tasks
- Delete existing tasks
- Clean, responsive web interface
- RESTful API endpoints

### Key Files:
- `app.py` - Flask application
- `test_app.py` - Unit tests
- `requirements.txt` - Python dependencies
- `templates/index.html` - Web interface
- `Dockerfile` - Container configuration

## 🔧 Prerequisites

- **Jenkins**: Latest LTS version
- **Python**: 3.8+
- **Docker**: Latest version
- **Kubernetes**: kubectl and cluster access
- **AWS CLI**: For Lambda deployments
- **Git**: Version control

## 🚦 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/ahmedalaa14/jenkins-project.git
cd jenkins-project
```

### 2. Choose Your Deployment Scenario
Navigate to any of the subdirectories and follow the specific deployment instructions:

```bash
# For basic Jenkins learning
cd jenkins-basics

# For Docker deployment
cd docker

# For Kubernetes deployment
cd kubernetes

# For serverless deployment
cd lambda-deployment

# For advanced CI/CD
cd 06-advanced-project
```

### 3. Set Up Jenkins Pipeline
1. Create a new Pipeline job in Jenkins
2. Configure the SCM to point to this repository
3. Set the Jenkinsfile path to the appropriate scenario
4. Configure required credentials (Docker Hub, AWS, K8s, etc.)

## 📋 Jenkins Credentials Required

Depending on the deployment scenario, you'll need to configure these credentials in Jenkins:

- `docker-hub-credentials` - Docker Hub login
- `kubeconfig-credentials-id` - Kubernetes cluster config
- `aws-access-key` - AWS access key
- `aws-secret-key` - AWS secret key
- `github-access-token` - GitHub token for releases

## 🧪 Testing

Each scenario includes comprehensive testing:
- **Unit Tests**: pytest-based Python tests
- **Acceptance Tests**: Node.js-based end-to-end tests
- **Integration Tests**: Environment-specific validation

Run tests locally:
```bash
pip install -r requirements.txt
pytest
```


