# 🚀 Static Website Hosting & Auto-Deployment with S3, Cloudflare & GitHub Actions

## 📌 Introduction
This project demonstrates how to host and automatically deploy a **static website** using **AWS S3 (Free Tier)** and **Cloudflare (Free)**, with deployments triggered on **GitHub commits**.  
It showcases a simple **CI/CD pipeline** that ensures any code change pushed to the repository is automatically reflected on the live site.

---

## 📖 Abstract
The goal was to create a cost-effective deployment pipeline using free-tier cloud services.  
- The static website was built with **HTML & CSS**.  
- **GitHub Actions** automates deployment.  
- **S3 bucket** stores the website contents.  
- **Cloudflare** provides a global CDN and free SSL (HTTPS).  

The final setup ensures that every GitHub push triggers an automated deployment to the live site.

---

## 🛠️ Tools Used
- **AWS S3** – Static file hosting (Free Tier)  
- **Cloudflare** – CDN, DNS, and HTTPS with free SSL  
- **GitHub Actions** – CI/CD workflow for automated deployment  
- **HTML/CSS** – Static website content  
- **Bash & AWS CLI** – For syncing files  

---

## ⚙️ Steps Involved in Building the Project

### 1. Create a Static Website
- Built a simple `index.html` and `style.css`.  
- Verified locally by opening `index.html` in a browser.  

### 2. Push Website Code to GitHub
- Initialized a Git repository.  
- Pushed the static site files to GitHub.  

### 3. Configure AWS S3
- Created an **S3 bucket** for hosting.  
- Enabled **static website hosting**.  
- Configured **bucket policy** to allow public read access.  
- Created an **IAM User with programmatic access** for GitHub Actions.  

### 4. Set Up GitHub Actions
- Created a workflow file in `.github/workflows/deploy.yml`.  
- Added `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` as GitHub Secrets.  
- Verified successful deployment by checking the S3 bucket.  

### 5. Integrate Cloudflare
- Connected GitHub repository to **Cloudflare Pages**.  
- Set build output directory to `/` (root).  
- Cloudflare automatically generated a free HTTPS-enabled URL:  
  `https://<project-name>.pages.dev`  

### 6. Test Auto-Deployment
- Made a change in `index.html`.  
- Committed and pushed to GitHub.  
- Verified that the live site was updated automatically with HTTPS.  

