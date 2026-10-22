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
<img width="736" height="83" alt="image" src="https://github.com/user-attachments/assets/2bafe393-2eee-4664-83ee-2e53ade19f4d" />


## Public and Private Subnets

<img width="736" height="83" alt="image" src="https://github.com/user-attachments/assets/472c71c1-6667-4d5f-8c98-cedfdd66a31e" />



## Public and Private Route tables

<img width="736" height="94" alt="image" src="https://github.com/user-attachments/assets/f85d9ca8-0e4f-4523-9a78-ba270430d4b3" />


## Internet Gateway

<img width="736" height="94" alt="image" src="https://github.com/user-attachments/assets/6bea680a-74b4-4174-b3df-bbfafcad5901" />


## Elastic IP addresses

<img width="736" height="94" alt="image" src="https://github.com/user-attachments/assets/d4de0079-7284-49d1-a40c-81e1f4be23b6" />


## NAT Gateways

<img width="736" height="94" alt="image" src="https://github.com/user-attachments/assets/2d0c4788-d6c1-472f-be10-da9552c4d62e" />


## Security Groups

<img width="736" height="114" alt="image" src="https://github.com/user-attachments/assets/44390e5b-ce67-473d-85b2-38a7bb7a72ca" />


### EC2 & AutoScaling Group
## Launch template

<img width="736" height="114" alt="image" src="https://github.com/user-attachments/assets/e63bc44a-56a5-4b35-b1ab-fedad26b6154" />


## AutoScaling Group

<img width="736" height="114" alt="image" src="https://github.com/user-attachments/assets/bacc1212-752b-4896-9298-5892b6df6851" />


### Target Group & Load Balancer
## Target Group

<img width="736" height="114" alt="image" src="https://github.com/user-attachments/assets/4aae7a6f-93ca-409c-b9fb-8b3b35d39439" />


## Load balancer

<img width="736" height="114" alt="image" src="https://github.com/user-attachments/assets/bee54eaa-c088-43fa-976e-0efa287c41d7" />


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

