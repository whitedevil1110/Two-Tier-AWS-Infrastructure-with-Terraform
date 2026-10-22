# 🏗️ Two-Tier AWS Infrastructure with Terraform  

![Two-Tier Architecture](https://imgur.com/X4dGBg6.gif)

## 📌 Overview  

This project demonstrates a **Two-Tier architecture on AWS** using **Terraform** for Infrastructure as Code (IaC). It follows a modular and security-enhanced approach to create a **scalable, secure, and maintainable** infrastructure.  

### ✅ Key Features  

- **Modular Architecture** – Reusable Terraform modules for better management  
- **Infrastructure as Code (IaC)** – Automate AWS resource provisioning  
- **Security Best Practices** – IAM roles, policies, and WAF integration  
- **Scalability & High Availability** – Auto Scaling, Load Balancing, and Route 53  
- **Database Integration** – Managed Amazon RDS deployment  
- **SSL & CDN Optimization** – Secure connections and content acceleration  

---

## 🚀 Getting Started

### Prerequisites

- **Terraform** >= 1.0.0
- **AWS CLI** configured with appropriate permissions
- **An AWS account** with sufficient IAM permissions

### 1️⃣ Clone the Repository  

```bash
git clone https://github.com/NotHarshhaa/DevOps-Projects
cd DevOps-Projects/DevOps-Project-11/
```  

### 2️⃣ Configure Variables

⚠️ **Important**: Before deploying, update the `variables.tfvars` file:
- Change `RDS-PWD` to a secure password
- Update `DOMAIN-NAME` to your actual domain
- Modify other values as needed for your environment

### 3️⃣ Initialize and Apply Terraform  

```bash
terraform init
terraform plan -var-file=variables.tfvars
terraform apply -var-file=variables.tfvars --auto-approve
```  
### VPC & Other Networking related Services
## VPC
(https://miro.medium.com/v2/resize:fit:736/0*bTcoJoGjlg6ama3c)

## Public and Private Subnets

https://miro.medium.com/v2/resize:fit:736/0*2VWNj0x3QI9FcHwm

## Public and Private Route tables

https://miro.medium.com/v2/resize:fit:736/0*p9tDNlLzWHy9X4Y2

## Internet Gateway

https://miro.medium.com/v2/resize:fit:736/0*6ETHLCPnh6ScG03w

## Elastic IP addresses

https://miro.medium.com/v2/resize:fit:736/0*gR3KFl_WY8e5ddzP

## NAT Gateways

https://miro.medium.com/v2/resize:fit:736/0*Ge6MwFoqlok3UBq4

## Security Groups

https://miro.medium.com/v2/resize:fit:736/0*Molv2WHfNmwfRmuJ

### EC2 & AutoScaling Group
## Launch template

https://miro.medium.com/v2/resize:fit:736/0*Q2Sd8xEyiah7Djdb

## AutoScaling Group

https://miro.medium.com/v2/resize:fit:736/0*C618R7r4U4-kmX3B

### Target Group & Load Balancer
## Target Group

https://miro.medium.com/v2/resize:fit:736/0*EsEEVf7ApGKkQTFe

## Load balancer

https://miro.medium.com/v2/resize:fit:736/0*QTCPt2j7Gd5OpURt

### Database
## Subnet Group for RDS

https://miro.medium.com/v2/resize:fit:736/0*rLHsMTvRh_sw4-rm

## RDS Cluster

https://miro.medium.com/v2/resize:fit:736/0*jKUP9f-xQhkbRy3M

### After Core Service, Deploy Service on Server

## Route53

https://miro.medium.com/v2/resize:fit:736/0*W0-Fvu87ANSGoUj4

## AWS Certificate Manager

https://miro.medium.com/v2/resize:fit:736/0*HdzXL7d29RUWzZ2z

## AWS Web Application Firewall

https://miro.medium.com/v2/resize:fit:736/0*N4z4VUhf2th8e36d

## CloudFront

https://miro.medium.com/v2/resize:fit:736/0*AQ3ZkMLau34YUSt2

## IAM Role

https://miro.medium.com/v2/resize:fit:736/0*94hZ3hfPQZ2AsRi2

## IAM Policy

https://miro.medium.com/v2/resize:fit:736/0*ch9SQWcsk39ILv0J

## IAM instance profile

https://miro.medium.com/v2/resize:fit:736/0*pRXh28MOhC4rEJcy

### TF State file and State lock

## Backend- TF State file stored on S3

https://miro.medium.com/v2/resize:fit:736/0*r5Rl9HOFrpnMdf88

## TF State lock file

https://miro.medium.com/v2/resize:fit:736/0*ylscrtYceyI1Sgna


Once the deployment is completed, you can enter your domain name in the browser to validate whether your servers are perfectly running or not.
As you can see in the below snippet, the Application is running

https://miro.medium.com/v2/resize:fit:736/0*yDhfH8HxGO1EK4AW
---
### 4️⃣ Cleanup (Destroy Infrastructure)  

```bash
terraform destroy -var-file=variables.tfvars --auto-approve
```  

---

## 🔧 Configuration Files

- **`main.tf`** - Main Terraform configuration with module calls
- **`variables.tf`** - Variable declarations
- **`variables.tfvars`** - Variable values (update these before deployment)
- **`backend.tf`** - Terraform backend and provider configuration
- **`modules/`** - Reusable Terraform modules

---

## 🏗️ Project Architecture Highlights  

### 🔹 **Networking & Security**  

✅ **VPC & Subnets** – Securely isolated environment for your application  
✅ **IAM & Role-Based Access Control** – Fine-grained security permissions  
✅ **AWS WAF** – Protect against common web threats  

### 🔹 **Compute & Scaling**  

✅ **Auto Scaling Group** – Dynamic scaling based on demand  
✅ **Application Load Balancer (ALB)** – Efficient traffic distribution  
✅ **EC2 Instances** – Reliable computing power  

### 🔹 **Storage & Database**  

✅ **Amazon RDS** – Managed database for scalability and reliability  
✅ **S3 Buckets** – Secure storage for application assets  

### 🔹 **Networking & Optimization**  

✅ **Amazon Route 53** – Scalable domain name system (DNS)  
✅ **Amazon CloudFront (CDN)** – Faster content delivery worldwide  
✅ **SSL/TLS Encryption** – Secure communication with ACM  

---

## 🛠️ Author & Community  

This project is crafted by **[Whitedevil](https://github.com/whitedevil1110)** 💡.  
I’d love to hear your feedback! Feel free to share your thoughts.  

📧 **Connect with me:**

- **GitHub**: [@whitedevil1110](https://github.com/whitedevil1110)  
- **Blog**:   
- **Telegram Community**:  
- **LinkedIn**:  

---

## ⭐ Support the Project  

If you found this helpful, consider **starring** ⭐ the repository and sharing it with your network! 🚀  

### 📢 Stay Connected  

