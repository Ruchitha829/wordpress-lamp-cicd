# WordPress Deployment on LAMP with Ansible and CI/CD

## Project Overview
This project automates the deployment of a WordPress site on an AWS EC2 instance using the LAMP stack (Linux, Apache, MySQL, PHP), Ansible for automation, and GitHub Actions for CI/CD.

## Technologies Used
- WordPress
- Apache2 (Web Server)
- MySQL (Database)
- PHP (Scripting Language)
- AWS EC2 (Cloud Instance)
- Ansible (Configuration Management)
- GitHub Actions (CI/CD)

## Setup Instructions

### 1. Launch EC2
Launch a new EC2 instance (Ubuntu), and note its public IP and key file.

### 2. Configure Inventory
Edit `inventory.ini` with your EC2 public IP and key file path.

### 3. Run Ansible Playbook
```bash
ansible-playbook -i inventory.ini playbook.yml
```

### 4. CI/CD
On each push to `main`, GitHub Actions runs the deployment workflow.

## Security Notes
- Never upload your `.pem` key to GitHub.
- Always set correct permissions (`chmod 400 my-key.pem`).

## Author
Ruchitha- DevOps Enthusiast

