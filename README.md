# GitLab CI/CD Pipeline - Automated Deployment to AWS EC2

Complete CI/CD pipeline reducing deployment time from 30 minutes to 3 minutes (90% improvement) with automated Docker builds and EC2 deployment.

## 🎯 Features

- **4-Stage Pipeline**: Build → Test → Push → Deploy
- **Automated Docker Builds**: Containerization in CI pipeline
- **Docker Hub Integration**: Automated image push
- **AWS EC2 Deployment**: SSH-based automated deployment
- **90% Deployment Time Reduction**: From 30min → 3min

## 🛠️ Technologies

- GitLab CI/CD, Docker, Docker Hub, AWS EC2, SSH/SCP, Bash Scripting

## 📁 Project Structure

├── .gitlab-ci.yml          # CI/CD pipeline configuration
├── Dockerfile              # Application containerization
├── deploy.sh              # EC2 deployment script
└── src/                   # Application source code

## 🚀 Pipeline Stages

### 1️⃣ Build Stage
- Builds Docker image from source code
- Tags image with commit SHA

### 2️⃣ Test Stage
- Runs automated tests
- Validates build integrity

### 3️⃣ Push Stage
- Pushes Docker image to Docker Hub
- Tags as 'latest' and commit SHA

### 4️⃣ Deploy Stage
- SSH into AWS EC2 instance
- Pulls latest image
- Stops old container
- Starts new container

## 📊 Results

- ⏱️ **90% faster deployments**: 30 minutes → 3 minutes
- 🔄 **Fully automated**: Zero manual intervention
- 🐛 **8 hours debugging**: Resolved runner config, Docker permissions, SSH issues
- ✅ **Production-ready**: Tested and deployed successfully


## 🐛 Challenges Solved

1. **GitLab Runner Registration**: Configured runner with proper Docker executor
2. **Docker Permission Errors**: Added gitlab-runner to docker group
3. **SSH Authentication**: Configured SSH keys as GitLab CI/CD variables
4. **Network Issues**: Configured security groups for EC2 access

## 📝 Key Learnings

- GitLab CI/CD pipeline design and optimization
- Docker-in-Docker configuration
- Secure credential management in CI/CD
- Troubleshooting CI/CD failures
- AWS EC2 deployment automation

## 🔐 Security

- SSH keys stored as GitLab CI/CD variables
- Docker Hub credentials secured
- EC2 security groups configured
- No hardcoded credentials in code

## Contact
For questions or feedback:

LinkedIn: https://www.linkedin.com/in/pavangupta29/
Email: pavangupta.devops2@gmail.com
GitHub: pavannn29
