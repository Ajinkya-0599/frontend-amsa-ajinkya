# AMSA Frontend Repository

This repository contains the **frontend code** for the AMSA project. The project is built using **Next.js**, and the deployment is fully automated using **CI/CD pipelines** to an **AWS EC2 instance**.

---

## Project Overview

- **Frontend Framework:** Next.js  
- **Backend Framework:** Node.js (API runs on port 3001)  
- **Server:** AWS EC2 (Ubuntu)  
- **Process Manager:** PM2  
- **Web Server:** Nginx (serves frontend static files)  

---

## Deployment & Automation

The project includes **two main YAML configuration files** for deployment and infrastructure:

1. **`amsa-stack.yml`**
   - Defines the infrastructure for the project.  
   - Can include **CloudFormation or Terraform** configuration for provisioning EC2 instances, security groups, and networking.  
   - Ensures repeatable and consistent environment setup.

2. **`deploy.yml`**
   - GitHub Actions workflow for **CI/CD deployment**.  
   - Automates:
     - Checking out frontend and backend repositories.
     - Installing dependencies and building the frontend.
     - Exporting static frontend files.
     - Installing backend dependencies and starting the backend with PM2.
     - Copying frontend static files to EC2 Nginx folder.
     - Restarting Nginx to apply changes.
     - Updating EC2 instance dynamically using tags.

---

## How to Run Locally

1. Clone the repository:
```bash
git clone https://github.com/Ajinkya-0599/frontend-amsa-ajinkya.git
cd frontend-amsa-ajinkya
