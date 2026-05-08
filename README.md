# 🚀 Interactive DevOps Stack using Ansible

An interactive DevOps stack installer built using Ansible that allows users to install only the required tools on Ubuntu servers.

This project is useful for DevOps Engineers, Cloud Engineers, Linux Administrators, and beginners who want to automate server setup quickly and efficiently.

---

# ✨ Features

✅ Interactive installation process  
✅ Latest version installation  
✅ User confirmation before every installation  
✅ Automatically skips unwanted tools  
✅ Lightweight and modular structure  
✅ Easy to customize  
✅ Beginner friendly  
✅ Production-ready project structure  

---

# 🔥 How It Works

During execution, the playbook asks before installing every tool.

Example:

```bash
Do you want to install Nginx? (yes/no)
If user enters:
yes
→ Tool gets installed
no
→ Tool gets skipped automatically and playbook moves to the next tool

This helps avoid unnecessary installations and keeps the server optimized.

📦 Supported Tools
Category	Tools
Web Servers	Nginx, Apache
Programming Languages	PHP, Python, Java, Node.js
Package Managers	npm
Databases	MySQL, PostgreSQL, MongoDB, Redis
Containers	Docker
Container Orchestration	Kubernetes (kubectl)
Version Control	Git
Monitoring	Prometheus, Grafana
Logging	ELK Stack
CI/CD	GitLab Runner
📁 Project Structure
interactive-devops-stack/
├── inventory.ini
├── playbook.yml
└── roles/
    └── devops_stack/
        ├── tasks/
        │   ├── apache.yml
        │   ├── docker.yml
        │   ├── elk.yml
        │   ├── git.yml
        │   ├── grafana.yml
        │   ├── java.yml
        │   ├── kubernetes.yml
        │   ├── main.yml
        │   ├── mongodb.yml
        │   ├── mysql.yml
        │   ├── nginx.yml
        │   ├── nodejs.yml
        │   ├── npm.yml
        │   ├── php.yml
        │   ├── postgresql.yml
        │   ├── prometheus.yml
        │   ├── python.yml
        │   └── redis.yml
        └── vars/
            └── main.yml
⚙️ Requirements
Ubuntu 22.04 / 24.04
Ansible installed
SSH access to server
Sudo privileges
Internet connection
🛠 Install Ansible
sudo apt update
sudo apt install ansible -y
🖥 Configure Inventory
inventory.ini
[servers]
server1 ansible_host=YOUR_SERVER_IP ansible_user=ubuntu

Example:

[servers]
server1 ansible_host=65.2.10.20 ansible_user=ubuntu
▶️ Run Playbook
ansible-playbook -i inventory.ini playbook.yml
📌 Example Output
Do you want to install Nginx? (yes/no): yes
→ Installing Nginx...

Do you want to install Docker? (yes/no): yes
→ Installing Docker...

Do you want to install MongoDB? (yes/no): no
→ Skipping MongoDB...
🧠 Advantages
Saves server resources
Avoids unnecessary installations
Faster setup process
Interactive automation
Easy for beginners
Reusable Ansible role structure
🚀 Future Improvements
Jenkins support
GitHub Actions Runner support
Docker Swarm setup
Kubernetes cluster setup
Auto SSL setup
CentOS/RHEL support
GUI support
Tool version selection support

