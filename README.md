# Ansible Learn Project

Ansible project for learning purposes, focusing on automation tasks such as software installation, configuration, 
and service management all executed within a VirtualBox virtual machine environment

## 1. Project Setup
- Creating an `ansible` folder to store all required files.

## 2. VirtualBox Environment Setup
  1. **Create a VirtualBox VM**:
    - Download and install VirtualBox.
    - Create a new VM and select Ubuntu as the operating system.

  2. **Configure SSH Access**:
    - Install OpenSSH Server:
      ```bash
      sudo apt update
      sudo apt install openssh-server
      sudo systemctl enable ssh
      sudo systemctl start ssh
      ```
  3. **Configure Network Settings***;

  4. ***Define the Inventory in Ansible**:
    Create an inventory file (e.g., inventory.ini) that includes your VM's details like port,username,password

## 3. Automation Tasks
- Modify file permissions as needed (e.g., setting correct permissions for configuration files).
- Use Ansible to install necessary software such as:
  - Web servers (e.g., Nginx etc)
  - Databases (e.g., MySQL, PostgreSQL)
  - Other dependencies

## 4. Building an Inventory
- Inventories organize managed nodes in centralized files.
- An inventory file provides Ansible with system information and network locations.
- Using an inventory file, Ansible can manage multiple hosts efficiently.

## 5. Playbooks & Roles
### Playbooks
- Playbooks are YAML-based automation blueprints that define the sequence of operations for configuration and deployment.
- A playbook consists of multiple plays executed in order.
- Example playbook tasks:
  - Installing required packages
  - Setting up configurations using roles

### Roles
- Organize tasks into roles for better modularity and reusability.
- Roles include:
  - **Webserver Role** (e.g., Nginx, Apache)
  - **Database Role** (e.g., MySQL, PostgreSQL)

## 6. Execution & Testing
- Run the playbook and verify that:
  - Installations and configurations are applied correctly.
  - Installed services (e.g., Nginx, database) are up and running.
- Perform necessary testing to ensure system stability.

### Testing Connectivity
To test connectivity to the managed host, run:

```bash
ansible -i ansible/inventory.ini ubuntu_vm -m ping
```

### Running the Playbook
To execute the playbook, use the following command:

```bash
ansible-playbook -i ansible/inventory.ini ansible/playbook.yml --ask-become-pass
```
(provide the password you use to login in your virtualbox)


###############################################################################################################
This project serves as a hands-on guide to learning Ansible by automating infrastructure setup and configuration.
