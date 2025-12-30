# Devops-command-sheet

📘 README.md — CDAC DevOps Master Command & Implementation Guide

Purpose
This repository documents end-to-end DevOps concepts, commands, and hands-on assignments performed as part of the CDAC DevOps curriculum, structured for:

📚 Exam revision (MCQ + Lab)

🧪 Hands-on execution

🧑‍💻 GitHub documentation & interviews

Rule
If a tool cannot be placed in the DevOps lifecycle, you don’t need it yet.

🔁 DevOps Mental Model (Burn This In) :

Plan → Code → Build → Test → Package → Deploy → Operate → Monitor

🖥️ Essential Linux Terminal Commands (Ubuntu)

Non-negotiable for labs

📂 File & Directory Operations:
```bash
pwd
ls -la
cd folder/
mkdir project
rm -rf folder
cp file1 file2
mv old new
```
📄 File Viewing & Editing:
```bash:
cat file
less file
nano file
vim file
touch file.txt
```
🔐 Permissions & Ownership
```bash
chmod +x script.sh
chmod 755 file
chown user:user file
```
📦 Package Management
```bash
sudo apt update
sudo apt upgrade
sudo apt install git docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

🌱 Git & GitHub (Version Control Backbone)
🔄 Basic Git Workflow
```bash
git init
git clone <repo_url>
git status
git add .
git commit -m "message"
git push origin main
git pull origin main
```
🌿 Branching
```bash
git branch feature
git checkout feature
git merge feature
```
🔐 Authentication (CDAC)

HTTPS + GitHub Token (mandatory)

SSH (optional / advanced)

⚙️ Jenkins (Continuous Integration Engine)
✅ Setup Checklist

Java installed

Runs on: http://localhost:8080

Admin user created

🏗 Job Types

Freestyle Project (CDAC favorite)

Pipeline (Declarative) – advanced

🔁 Freestyle Job Flow

1.Source Code → GitHub

2.Build Step → Shell Script

3.Output → Console Logs

```bash
echo "Build successful"
chmod +x app.sh
./app.sh
```
📄 Jenkinsfile (Know This)
```bash
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello CDAC'
      }
    }
  }
}
```

🏗 Terraform (Infrastructure as Code)
📁 Core Files:
```hcl
main.tf
variables.tf
outputs.tf
terraform.tfstate
```

🛠 Core Commands
```bash
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy
```
🌩 AWS Provider Example
```hcl
provider "aws" {
  region = "ap-south-1"
}
```

🐳 Docker (Containerization)
📄 Dockerfile
```bach
FROM ubuntu
RUN apt update
CMD ["echo", "Hello DevOps"]
```

🛠 Commands
```bash
docker build -t myapp .
docker run myapp
docker ps
docker images
docker stop <container_id>
```


🚀 CDAC DevOps — Hands-On Assignment Playbook
1️⃣ GitHub Assignment (Foundation)
Objective

Create repository

Perform Git operations from Ubuntu

Push code successfully

Steps Performed

```bash
sudo apt update
sudo apt install git -y
git config --global user.name "Renold"
git config --global user.email "your_email@gmail.com"
git clone https://github.com/<username>/<repo>.git
cd <repo>
touch app.sh
nano app.sh
chmod +x app.sh
git add .
git commit -m "Initial commit"
git branch -M main
git push origin main
```


2️⃣ Jenkins CI Assignment
```bash
sudo apt install openjdk-17-jdk -y
sudo apt install jenkins -y
sudo systemctl start jenkins
sudo systemctl enable jenkins
```
Access:
```bash
http://localhost:8080
```
✔ Dashboard loaded
✔ Freestyle job executed
✔ Automation verified

3️⃣ Terraform IaC Assignment
```bash
sudo apt install terraform -y
mkdir terraform-lab && cd terraform-lab
nano main.tf
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy
```
✔ Infra created
✔ State tracked
✔ Reproducible

4️⃣ Docker Assignment
```bash
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker build -t cdac-docker .
docker run cdac-docker
```

5️⃣ AWS IAM + EC2 Assignment

IAM User: devops-engineer-user

Policies:

  EC2FullAccess

  S3FullAccess (if required)

  IAMReadOnlyAccess

EC2:

  Type: t3.micro

  Region: ap-south-1

```bash
ssh -i devops-lab-key.pem ec2-user@<public-ip>
aws sts get-caller-identity
```
✔ Role assumed
✔ No access keys
✔ Secure practice followed

🔒 Final CDAC Rule (Tattoo This)

IAM Roles > Access Keys
Root User = NEVER

