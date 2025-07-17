# VProfile Local Infrastructure - DevOps Portfolio Project

[![Vagrant](https://img.shields.io/badge/Vagrant-1563FF?style=flat&logo=vagrant&logoColor=white)](https://www.vagrantup.com/)
[![VMware](https://img.shields.io/badge/VMware-607078?style=flat&logo=vmware&logoColor=white)](https://www.vmware.com/)
[![Shell](https://img.shields.io/badge/Shell_Script-121011?style=flat&logo=gnu-bash&logoColor=white)](https://www.gnu.org/software/bash/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)](https://nginx.org/)

## 🎯 Project Overview

This project demonstrates **automated multi-tier infrastructure provisioning** using modern DevOps practices. It showcases my ability to orchestrate complex backend environments with **Infrastructure as Code (IaC)** principles.

### 🎓 Learning Context
*This project was completed as part of the "DevOps Beginners to Advanced with Projects" course by Imran Teli, serving as a hands-on learning artifact to demonstrate practical DevOps skills.*

## 🚀 Key Achievements

- ✅ **Automated VM lifecycle management** with Vagrant
- ✅ **Multi-service orchestration** using shell scripting
- ✅ **Zero-manual configuration** deployment process
- ✅ **Production-ready service stack** simulation
- ✅ **Mac M1/M2 compatibility** with VMware integration

## 🛠️ Technology Stack

| Category | Technology | Purpose |
|----------|------------|---------|
| **Virtualization** | VMware + Vagrant | VM lifecycle management |
| **Automation** | Shell Scripts | Service provisioning |
| **Database** | MySQL/MariaDB | Data persistence |
| **Caching** | Memcached | Performance optimization |
| **Message Queue** | RabbitMQ | Asynchronous communication |
| **Application Server** | Apache Tomcat | Java application hosting |
| **Web Server** | Nginx | Reverse proxy & load balancing |

## 🎯 Project Objectives

Simulate a complete backend infrastructure using multiple VMs, with automated provisioning of each service using Vagrant and Shell scripts.

This project demonstrates:
- 🔧 **Infrastructure automation** using Vagrant
- 🐧 **Linux system administration** via shell scripting
- 🏗️ **Multi-tier backend service deployment**
- 🌐 **Network and firewall configuration**
- ☕ **WAR build and deployment** of a Java Spring application

## 🏗️ Architecture Overview

![Infrastructure Diagram](./assets/infra.png)

### Infrastructure Components
- **Frontend Layer**: Nginx (Load Balancer & Reverse Proxy)
- **Application Layer**: Apache Tomcat (Java Application Server)
- **Caching Layer**: Memcached (Performance Optimization)
- **Message Queue**: RabbitMQ (Asynchronous Communication)
- **Database Layer**: MySQL/MariaDB (Data Persistence)

## ⚙️ Prerequisites

Make sure the following are installed on your system:
- **VMware Workstation/Fusion**
- **Vagrant**
- **Git Bash** or compatible terminal
- **Hostmanager plugin**:

```bash
vagrant plugin install vagrant-hostmanager
```

## 🚀 Getting Started

1. **Clone this project:**

```bash
git clone https://github.com/egnicolas/vprofile-infra-portfolio.git
cd vprofile-infra-portfolio
cd vagrant/Manual_provisioning
```

2. **Boot up the environment (automated):**

```bash
vagrant up
```

This command will launch all five VMs and execute provisioning scripts automatically.

## 🔧 Automated Service Provisioning

Each service is provisioned through automated shell scripts triggered by the Vagrantfile.

**Provisioned components:**
1. **MySQL (db01)** – Automated MariaDB install, schema import, port open
2. **Memcached (mc01)** – Installed and configured on port 11211
3. **RabbitMQ (rmq01)** – Auto-installed with default admin user
4. **Tomcat + Java + Maven (app01)** – WAR deployed with build via Maven
5. **Nginx (web01)** – Reverse proxy config applied automatically

## 🌍 Accessing the Application

Once all VMs are up, access the deployed app via:

```
http://web01
```

*Note: You may need to update your `/etc/hosts` file based on local VM IPs.*

## 📁 Project Structure

```
vprofile-infra-portfolio/
└── vagrant/
    └── Manual_provisioning/
        ├── Vagrantfile
        ├── shell-scripts/
        └── README.md
```

## 🧠 Why This Project?

This project reflects my skills in:
- **Infrastructure automation** with Vagrant + Shell
- **Linux provisioning and configuration**
- **Multi-VM orchestration**
- **Basic networking and firewall setup**
- **Java backend deployment practices**

It serves as a hands-on demonstration of core DevOps concepts.

## 🏁 Next Steps

- Improve infrastructure by using declarative IaC tools like Ansible or Terraform
- Integrate CI/CD pipelines for continuous delivery
- Add monitoring and alerting (e.g., Prometheus, Grafana)
- Add infrastructure diagrams and architecture screenshots
