# 🌟 AMSA Website  

![Project Banner](https://via.placeholder.com/1200x300?text=AMSA+Website+Project)  

**AMSA** is a full-stack web application designed to manage and showcase AMSA activities, events, and member engagement.  
It uses a modern Next.js frontend, a Node.js backend, automated CI/CD pipeline, and secure AWS-based deployment.  

---

## 🚀 Features  

- ⚡ **Fast Frontend**: Next.js for optimized builds and performance  
- 🔧 **Backend API**: Node.js + Express for business logic and APIs  
- 🛠️ **CI/CD Pipeline**: Automated builds and deployments via GitHub Actions  
- 🌍 **CloudFront CDN**: Global delivery of static frontend assets  
- 📊 **Monitoring & Alerts**: Server health and error tracking via AWS CloudWatch  
- ☁️ **AWS Hosting**: Frontend + Backend deployed on AWS EC2  
- 🔐 **Secure by Default**: HTTPS + SSL certificates  

---

## 🗂 Project Structure  

amsa-website/
├── CloudFormation/ # AWS infrastructure templates
├── frontend/ # Next.js frontend
├── backend/ # Node.js backend
├── .github/workflows/ # CI/CD pipeline
└── README.md # Documentation


---

## 🛠️ Tech Stack  

| Component   | Technology                     |
|-------------|--------------------------------|
| Frontend    | Next.js                         |
| Backend     | Node.js, Express               |
| Hosting     | AWS EC2                        |
| CDN         | AWS CloudFront                 |
| CI/CD       | GitHub Actions                 |
| Monitoring  | AWS CloudWatch / Dashboards    |
| Security    | HTTPS / SSL Certificates       |

---

## 🏗️ Architecture Overview  

- **GitHub Actions** → Builds, tests, and deploys frontend + backend  
- **EC2 Instances** → Hosts frontend and backend servers  
- **CloudFront CDN** → Caches frontend for global performance  
- **Monitoring** → Tracks uptime, CPU, memory, network, and errors  

---

## 📦 Deployment Process  

### 1️⃣ CloudFormation (IaC)  
- Spins up EC2 instances for frontend & backend  
- Configures networking, ports, and security groups  
- Sets up CloudFront distribution  

### 2️⃣ CI/CD (GitHub Actions)  
- Triggered on `push` to `main`  
- **Frontend:** Install → Build → Export → Deploy to EC2  
- **Backend:** Install → Deploy with `pm2`  

### 3️⃣ Monitoring & Alerts  
- CloudWatch dashboards for performance  
- Alerts via Email / Slack  

### 4️⃣ Manual Deployment (first time setup)  

**Frontend**
```bash
cd frontend
npm install
npm run build
npm run export

# Copy build to EC2
scp -r out/ ubuntu@<FRONTEND_EC2_IP>:/var/www/frontend-amsa-ajinkya

🏷️ Badges






