# 🚀 Ansible LAMP Stack Deployment on AWS

## 📌 Overview

This project automates the deployment of a production-ready **LAMP stack (Linux, Apache, MySQL, PHP)** on AWS EC2 instances using Ansible.

It demonstrates Infrastructure as Code (IaC), configuration management, and secure DevOps practices.

---

## 🏗 Architecture

* **1 Control Node and web Server(Public Subnet)**
* Runs Ansible and manages all servers
* 🌐 Web Server (Apache)

* **3 Managed Nodes (Private Subnet)**

  
  * ⚙️ App Server (PHP)
  * 🗄 Database Server (MySQL)

---

## ⚙️ Features

* Modular design using **Ansible Roles**
* Centralized configuration using **group_vars**
* Dynamic deployment using **Jinja2 templates**
* Secure secrets using **Ansible Vault**
* Conditional execution using **when**
* Iteration using **loops**
* Selective execution using **tags**
* Error handling using **block / rescue / always**
* Service health checks using **register + debug**
* Idempotent automation

---

## 📁 Project Structure

```
ansible-project/
├── inventory/
│   └── hosts.ini
├── group_vars/
│   ├── all.yml
│   ├── webservers.yml
│   └── dbservers.yml
├── roles/
│   ├── common/
│   ├── webserver/
│   ├── appserver/
│   └── database/
├── site.yml
├── ansible.cfg
```

---

## 🔐 Security

Sensitive data (like DB password) is encrypted using **Ansible Vault**

### Run with Vault:

```
ansible-playbook site.yml --vault-password-file ~/.vault
```

---

## 🚀 How to Run

### Full deployment:

```
ansible-playbook site.yml
```

### Run only web server:

```
ansible-playbook site.yml --tags web
```

---

## 🧠 Key Learnings

* Infrastructure as Code (IaC)
* Configuration Management using Ansible
* Secure credential handling (Vault)
* Debugging automation workflows
* Multi-tier architecture deployment

---

## 🎯 Outcome

Automated deployment of a scalable multi-tier application using Ansible with secure, reusable, and modular design.

---

## 👨‍💻 Author

**Arti Semwal**

---

## ⭐ Future Improvements

* CI/CD using GitHub Actions
* Terraform integration
* Monitoring (Prometheus/Grafana)
* Load balancer setup
* Docker containerization

---
