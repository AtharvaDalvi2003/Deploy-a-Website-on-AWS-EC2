# 🌐 Website Deployment on AWS EC2

## 📌 Problem Statement
Many learners and startups face difficulty understanding the steps involved in cloud-based hosting and configuring web servers for live deployment.

## 🎯 Objective
To launch an EC2 instance on AWS, install and configure a web server (Apache or Nginx), and deploy a static HTML/CSS website that is publicly accessible over the internet.

---

## 🧰 Requirements

- ✅ AWS Account
- ✅ EC2 Instance (Ubuntu 20.04 or Amazon Linux 2)
- ✅ SSH Access / Terminal
- ✅ Apache or Nginx Web Server
- ✅ Basic HTML/CSS Files

---

## 🚀 Steps to Deploy

### 1. **Launch EC2 Instance**
- Go to the AWS EC2 Dashboard
- Click "Launch Instance"
- Select Ubuntu Server 20.04 (or Amazon Linux 2)
- Choose instance type (e.g., t2.micro)
- Configure security group:
  - Allow **SSH (22)** and **HTTP (80)** access from anywhere (0.0.0.0/0)

### 2. **Connect to EC2 via SSH**
```bash
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
```
3. Install Apache (or Nginx)
Apache:
```

sudo apt update
sudo apt install apache2 -y
```
Nginx (alternative):
```
sudo apt update
sudo apt install nginx -y
```
4. Upload Your Website Files
You can use ```scp``` (from your local machine) to transfer HTML/CSS files:
```
scp -i "your-key.pem" index.html style.css ubuntu@your-ec2-public-ip:/tmp
```
5. Verify Deployment
Go to:
``` 
http://your-ec2-public-ip 
```
You should see your website live!

📂 Project Structure
```
ec2-website-deployment/
├── index.html           # Homepage
├── style.css            # Stylesheet
├── README.md            # Project documentation
```
## 📸 Screenshots

### 🏠 Home Page
<img width="1906" height="927" alt="Image" src="https://github.com/user-attachments/assets/803cffda-ae57-47ba-b951-2c30f38a9b54" />


### 👤 About Page
<img width="1905" height="923" alt="Image" src="https://github.com/user-attachments/assets/5052e4cc-0d7f-4c6f-b45b-c2492bd727ff" />


### 📬 Contact Page
<img width="1900" height="922" alt="Image" src="https://github.com/user-attachments/assets/3214bf5b-e2c8-430a-a24c-db1d774690d7" />


### ✅ Outcome
A basic HTML/CSS website successfully deployed and hosted on a cloud server using Amazon EC2 and Apache (or Nginx), demonstrating foundational DevOps and cloud deployment skills.

### 🔐 Security Tip
Once your website is live:

- Consider removing public SSH access if not needed
- Restrict inbound traffic to specific IPs
- Enable automatic updates for security patches

### 📄 License
MIT License – Open to use and modify.
