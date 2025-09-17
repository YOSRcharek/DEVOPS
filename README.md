# ⚡ CI/CD Automation with Jenkins

[![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-blue?logo=jenkins&logoColor=white)](https://www.jenkins.io/)
[![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![SonarQube](https://img.shields.io/badge/SonarQube-Code%20Quality-4E9BCD?logo=sonarqube&logoColor=white)](https://www.sonarqube.org/)
[![Nexus](https://img.shields.io/badge/Nexus-Artifacts-orange?logo=sonatype&logoColor=white)](https://www.sonatype.com/)
[![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-E6522C?logo=prometheus&logoColor=white)](https://prometheus.io/)
[![Grafana](https://img.shields.io/badge/Grafana-Dashboard-F46800?logo=grafana&logoColor=white)](https://grafana.com/)
[![JUnit](https://img.shields.io/badge/JUnit-Testing-green?logo=java&logoColor=white)](https://junit.org/)

---

## 📄 Project Overview
This project implements a **complete CI/CD pipeline** using **Jenkins**, automating the build, test, analysis, packaging, and deployment of an application.  
The pipeline ensures:
- ✅ Continuous Integration with **JUnit** & **Mockito** unit testing  
- 🔍 Code Quality checks with **SonarQube**  
- 📦 Artifact management via **Nexus** repository  
- 🐳 Containerization with **Docker** & orchestration using **Docker Compose**  
- 📊 Monitoring and metrics visualization with **Prometheus** and **Grafana**

---

## 🚀 Technologies
| Technology | Purpose |
|------------|--------|
| ⚙️ **Jenkins** | CI/CD automation |
| 🐳 **Docker & Docker Compose** | Build & run containers |
| 🔍 **SonarQube** | Code quality analysis |
| 📦 **Nexus Repository** | Artifact storage |
| 🧪 **JUnit & Mockito** | Unit testing |
| ☕ **Maven** | Build & dependency management |
| 📊 **Prometheus & Grafana** | Monitoring & visualization |
| 🖥️ **Vagrant** | VM provisioning for local infrastructure |

---

## 🔧 Prerequisites
Before running this project, make sure the following tools are installed and configured:

- [Vagrant](https://developer.hashicorp.com/vagrant) 🖥️  
  - Used to create a virtual environment with all CI/CD tools pre-installed.  
- [VirtualBox](https://www.virtualbox.org/) 💻 (or any Vagrant-supported provider)  
- [Docker](https://www.docker.com/) 🐳  
- [Jenkins](https://www.jenkins.io/) ⚙️  
- [SonarQube](https://www.sonarqube.org/) 🔍  
- [Nexus Repository Manager](https://www.sonatype.com/) 📦  
- [Prometheus](https://prometheus.io/) 📊  
- [Grafana](https://grafana.com/) 📈  
- [Maven](https://maven.apache.org/) ☕  
- Java 11 or later ☕ (for Maven/Jenkins builds)

> ⚠️ **Tip:** Vagrant can be configured to provision all of these services automatically using a `Vagrantfile`.

---

## ⚡ Pipeline Workflow
1. **Source Code Checkout** – Jenkins pulls code from GitHub.  
2. **Build & Test** – Maven builds the project, runs unit tests (JUnit & Mockito).  
3. **Static Code Analysis** – SonarQube scans for bugs, vulnerabilities, and code smells.  
4. **Artifact Packaging** – Maven packages the app and uploads artifacts to Nexus.  
5. **Containerization** – Docker builds images and pushes them to Docker Hub.  
6. **Deployment** – Docker Compose deploys containers to the target environment.  
7. **Monitoring** – Prometheus collects metrics, Grafana visualizes dashboards.

---
├── Jenkinsfile # CI/CD pipeline definition
├── Vagrantfile # Vagrant configuration for provisioning environment
├── docker-compose.yml # Docker Compose services (app, Prometheus, Grafana, etc.)
├── pom.xml # Maven build configuration
└── src/ # Application source code


---

## 🏁 Setup & Execution

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/YOSRcharek/DEVOPS.git
cd DEVOPS
```
### 2️⃣ Start the Virtual Environment

Provision a VM with all required tools:
```bash
vagrant up
```

This will:

Install Jenkins, SonarQube, Nexus, Prometheus, and Grafana.

Configure Docker & Maven.

### 3️⃣ Access Services
Service	URL	Default Credentials
Jenkins	http://localhost:8080
	admin / (initial password in /var/lib/jenkins/secrets/initialAdminPassword)
SonarQube	http://localhost:9000
	admin / admin
Nexus	http://localhost:8081
	admin / admin123
Prometheus	http://localhost:9090
	N/A
Grafana	http://localhost:3000
	admin / admin
### 4️⃣ Run the Pipeline

Open Jenkins → Create a new Pipeline job → Point to the Jenkinsfile in the repository.

Trigger a Build and watch the automated stages:

Build → Test → Analyze → Package → Deploy → Monitor

📊 Monitoring

Prometheus collects real-time metrics from the application and Docker containers.

Grafana provides interactive dashboards to visualize CPU usage, memory, build history, and deployment status.

🔮 Future Improvements

🌐 Kubernetes integration for production-grade orchestration.

🔑 Vault integration for secrets management.

🔁 Blue/Green and Canary deployment strategies.

🚦 Automated rollback on failed builds.

### 📜 License

This project is released under the MIT License
.

### 💡 GitHub Repository

🔗 DEVOPS


### ✅ Highlights
- Uses **icons/badges** for technologies (Flutter-style GitHub README).
- Clearly lists **prerequisites** (Vagrant + all services).
- Shows **service URLs & default credentials** for quick access.
- Includes **pipeline workflow** for easy understanding.
