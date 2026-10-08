# 🚀 Azure VM Nginx Web Server Deployment

## 📌 Project Overview

This project demonstrates the deployment of a Linux-based web server on Microsoft Azure using an Ubuntu Virtual Machine and Nginx.

The project was completed as part of my Cloud Engineer practical learning journey and focuses on real-world cloud infrastructure, networking, Linux server administration, remote access, security rules, and web server deployment.

The objective was to provision an Azure Virtual Machine, configure its networking, securely access the Linux server using SSH, install Nginx, and successfully expose a web server to the internet.

---

# 🎯 Project Objectives

* Deploy an Ubuntu Linux Virtual Machine on Microsoft Azure
* Create and configure Azure networking resources
* Configure Virtual Network and Subnet
* Configure Network Security Group rules
* Enable secure SSH remote access
* Configure Public IP connectivity
* Perform Linux server administration
* Update Ubuntu packages
* Install and manage Nginx
* Verify web server availability
* Access the web server through the public internet

---

# 🏗️ Architecture

```text
                         Internet
                            │
                            │ HTTP : 80
                            ▼
                     Public IP Address
                            │
                            ▼
                  Network Security Group
                     │              │
                 SSH : 22        HTTP : 80
                     │              │
                     └──────┬───────┘
                            ▼
                     Virtual Network
                            │
                            ▼
                         Subnet
                            │
                            ▼
                   Network Interface
                            │
                            ▼
                  Azure Virtual Machine
                            │
                            ▼
                     Ubuntu Linux
                            │
                            ▼
                         Nginx
                            │
                            ▼
                    Web Server Content
```

---

# ☁️ Azure Resources

The project includes the following Azure resources:

* Resource Group
* Virtual Machine
* Virtual Network
* Subnet
* Network Security Group
* Network Security Rules
* Public IP Address
* Network Interface
* Managed OS Disk
* System Assigned Managed Identity
* Azure Monitor Alerts
* VM Tags

---

# 🖥️ Virtual Machine Configuration

| Configuration    | Details                 |
| ---------------- | ----------------------- |
| Cloud Provider   | Microsoft Azure         |
| Operating System | Ubuntu Server 24.04 LTS |
| VM Size          | Standard D2plds v6      |
| vCPUs            | 2                       |
| Memory           | 4 GiB                   |
| Authentication   | SSH Public Key          |
| Disk             | Standard SSD            |
| Region           | Central US              |
| Web Server       | Nginx                   |
| Web Protocol     | HTTP                    |
| HTTP Port        | 80                      |
| SSH Port         | 22                      |

---

# 🔐 Security Configuration

The Network Security Group was configured with inbound security rules for:

### SSH

```text
Port: 22
Protocol: TCP
Purpose: Secure remote administration
```

### HTTP

```text
Port: 80
Protocol: TCP
Purpose: Web traffic
```

The SSH private key was securely stored locally and was not uploaded to GitHub.

---

# 🔑 SSH Remote Access

The Azure Virtual Machine was accessed remotely from Windows PowerShell using SSH.

Example:

```bash
ssh -i ./vm-web-01-key.pem azureadmin@PUBLIC_IP
```

SSH was used to securely connect to the Ubuntu Linux server.

---

# 🐧 Linux Server Administration

After connecting to the VM, the server was verified using:

```bash
hostname
```

```bash
whoami
```

```bash
lsb_release -a
```

```bash
uptime
```

The Ubuntu package repository was updated:

```bash
sudo apt update
```

Installed packages were upgraded:

```bash
sudo apt upgrade -y
```

---

# 🌐 Nginx Installation

Nginx was installed using:

```bash
sudo apt install nginx -y
```

The Nginx service was verified using:

```bash
sudo systemctl status nginx
```

The service was successfully confirmed as:

```text
Active: active (running)
```

---

# 🧪 Deployment Verification

The web server was tested using the Azure VM Public IP address.

```text
http://PUBLIC_IP
```

The Nginx Welcome Page was successfully displayed in the web browser.

This confirmed:

* Azure VM was running
* Ubuntu Linux was operational
* Nginx was running
* Port 80 was accessible
* NSG HTTP rule was working
* Public IP connectivity was working

---

# 🧠 Key Concepts Learned

* Azure Virtual Machines
* Ubuntu Linux
* Resource Groups
* Virtual Networks
* Subnets
* Network Security Groups
* Inbound Security Rules
* Public IP Addresses
* Network Interfaces
* SSH
* SSH Key Authentication
* Linux Package Management
* Linux System Administration
* Nginx
* HTTP
* TCP
* Port 22
* Port 80
* Azure Monitoring
* Cloud Resource Tags

---

# 🏢 Real-World Cloud Engineer Use Case

In a real company environment, Cloud Engineers may be responsible for:

* Provisioning cloud virtual machines
* Configuring Linux servers
* Managing cloud networking
* Securing network traffic
* Configuring SSH access
* Deploying web servers
* Managing Nginx
* Monitoring infrastructure
* Troubleshooting connectivity
* Verifying production deployments

This project represents a simplified real-world workflow for deploying and managing a Linux-based web server in Microsoft Azure.

---

# 🔧 Troubleshooting Areas

During this project, the following troubleshooting concepts were practiced:

* SSH connectivity
* Public IP connectivity
* NSG inbound rules
* Port 22 access
* Port 80 access
* Linux service status
* Nginx service verification
* Azure VM status
* Browser connectivity testing

---

# 📈 Future Improvements

The next phase of this project will include:

* Replace the default Nginx page
* Deploy a custom HTML website
* Configure Nginx server blocks
* Configure DNS
* Enable HTTPS with SSL/TLS
* Configure HTTPS port 443
* Implement better SSH security
* Configure Azure Monitor
* Configure VM alerts
* Add automated deployment
* Automate infrastructure using Terraform
* Automate configuration using Ansible
* Integrate CI/CD

---

# 👨‍💻 Author

**Usman Bari**

Cloud Engineer Learning Journey

Focused on:

* Microsoft Azure
* Cloud Computing
* Linux
* Infrastructure Automation
* Ansible
* Terraform
* Docker
* Kubernetes
* CI/CD

---

# ⭐ Project Status

✅ Azure VM Deployed

✅ Ubuntu Linux Configured

✅ SSH Remote Access Configured

✅ Azure Networking Configured

✅ NSG Security Rules Configured

✅ Nginx Installed

✅ Web Server Running

✅ Website Successfully Tested

🚧 Custom Website Deployment — Next Step

---

# 📌 Final Result

Successfully deployed and tested a Linux-based Nginx web server on Microsoft Azure.

This project demonstrates practical skills in cloud infrastructure provisioning, Azure networking, Linux administration, SSH remote access, security configuration, and web server deployment.
# azure-vm-nginx-web-server
Deploying an Ubuntu Linux web server on Microsoft Azure with SSH, Azure networking, NSG security rules, and Ngin
