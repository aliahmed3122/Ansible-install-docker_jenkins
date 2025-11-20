# 🚀 Ansible Playbook for Installing Docker and Jenkins

This Ansible playbook automates the installation of **Docker** and **Jenkins** on both **Ubuntu** and **RedHat-based** systems.

---

## 📌 Requirements

### 🔹 Control Node:
- Ansible installed (`ansible` command available).
- SSH access to the target machines.

### 🔹 Managed Nodes (Target Machines):
- **OS:** Ubuntu or RedHat-based distributions (CentOS, RHEL, Rocky Linux).
- Sudo privileges enabled.

---

## 📌 Features

✅ **Automated Installation** – Installs Docker and Jenkins with a single command.  
✅ **OS Detection** – Supports **Ubuntu** and **RedHat-based** distributions.  
✅ **Dependency Management** – Installs required dependencies before proceeding.  
✅ **Repository Setup** – Adds official Docker and Jenkins repositories.  
✅ **Service Management** – Ensures Docker and Jenkins are enabled and running.  
✅ **Secure Execution** – Uses `sudo` for privileged tasks with `--ask-become-pass`.  
✅ **Modular Roles** – Organized using **Ansible roles** for maintainability.  
✅ **Idempotency** – Only changes what’s necessary, avoiding redundant installations.  

---

## 📂 Playbook Structure

```plaintext
ansible/
│── ansible.cfg         # Ansible configuration file
│── inventory           # List of target hosts
│── main.yml            # Main playbook file
└── roles/              # Role-based structure
    ├── docker/         # Docker installation role
    │   ├── tasks/      # Tasks for installing Docker
    │   ├── handlers/   # Handlers for Docker service
    │   ├── defaults/   # Default variables
    │   └── README.md   # Role-specific documentation
    └── jenkins/        # Jenkins installation role
        ├── tasks/      # Tasks for installing Jenkins
        ├── handlers/   # Handlers for Jenkins service
        ├── defaults/   # Default variables
        └── README.md   # Role-specific documentation
```
---
## Run Playbook 
```sh
  $ ansible-playbook main.yml --ask-become-pass
```
---

## 🎯 Conclusion

This playbook simplifies the setup of **Docker** and **Jenkins** using **Ansible**, making deployments **faster** and **more reliable**. 🚀  
With just a single command, you can automate the installation and configuration across multiple systems effortlessly.  


