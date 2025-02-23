# Ansible Learn Project

Ansible project for learning purposes, focusing on automation tasks such as software installation, configuration, and service management.

## 1. Project Setup
- Creating an `ansible` folder to store all required files.

## 2. Automation Tasks
- Modify file permissions as needed (e.g., setting correct permissions for configuration files).
- Use Ansible to install necessary software such as:
  - Web servers (e.g., Nginx etc)
  - Databases (e.g., MySQL, PostgreSQL)
  - Other dependencies

## 3. Building an Inventory
- Inventories organize managed nodes in centralized files.
- An inventory file provides Ansible with system information and network locations.
- Using an inventory file, Ansible can manage multiple hosts efficiently.

## 4. Playbooks & Roles
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

## 5. Execution & Testing
- Run the playbook and verify that:
  - Installations and configurations are applied correctly.
  - Installed services (e.g., Nginx, database) are up and running.
- Perform necessary testing to ensure system stability.

---
This project serves as a hands-on guide to learning Ansible by automating infrastructure setup and configuration.
