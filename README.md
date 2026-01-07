# GlobalMart CI/CD Pipeline

 📌 Project Overview

GlobalMart CI/CD is an end-to-end **Continuous Integration and Continuous Deployment (CI/CD)** pipeline built using **GitHub Actions** and **AWS EC2**.
The pipeline automatically deploys a web application to an **Apache HTTP Server** whenever changes are pushed to the GitHub repository.

This project demonstrates real-world DevOps practices, including infrastructure setup, automation, and deployment using a **self-hosted GitHub Actions runner**.
## 🛠️ Tech Stack

* **AWS EC2** (Amazon Linux 2023)
* **Apache HTTP Server**
* **GitHub Actions**
* **Self-Hosted GitHub Runner**
* **Linux (Bash)**
* **HTML**
 🏗️ Architecture
Developer → GitHub Repository → GitHub Actions Workflow
                                      |
                                      ↓
                         Self-Hosted Runner on EC2
                                      |
                                      ↓
                            Apache Web Server

 🚀 CI/CD Workflow

1. Developer pushes code to the `main` branch
2. GitHub Actions workflow is triggered
3. Job is picked up by the **self-hosted runner on EC2**
4. `index.html` is deployed to `/var/www/html`
5. Apache service is restarted automatically
6. Updated website is served via EC2 public IP

 📂 Repository Structure

```
GlobalMart-CICD/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── index.html
├── README.md
```
## ⚙️ GitHub Actions Workflow

The workflow runs on every push to `main` and performs:

* Repository checkout
* File deployment to Apache web root
* Permission handling
* Apache service restart
* Health verification
* 
## ✅ Features

* Fully automated deployment
* No manual SSH or file copy required
* Uses **free-tier friendly** self-hosted runner
* Real-time CI/CD validation
* Production-style setup
* 
## 🔐 Security Considerations

* SSH access restricted via Security Groups
* GitHub runner uses scoped registration token
* No credentials stored in repository

## 📈 Learning Outcomes

* Implemented CI/CD using GitHub Actions
* Configured and managed self-hosted runners
* Troubleshot Linux and .NET dependency issues
* Automated deployments on AWS EC2
* Gained hands-on DevOps experience

## 📸 Proof of Execution

* Successful GitHub Actions workflow runs (green checks)
* Automatic updates reflected on EC2 public IP
* No manual intervention required

## 🧹 Cost Management

* EC2 instance can be **stopped** when not in use
* No paid GitHub Actions runners used
* Suitable for AWS Free Tier usage

## 🏁 Conclusion

This project successfully demonstrates a **real-world CI/CD pipeline** using industry-standard tools. It reflects practical DevOps skills applicable to Cloud Support, DevOps, and Software Engineering roles.

## 👩‍💻 Author

**Srividya Mekala**
Cloud & DevOps Enthusiast
