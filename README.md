<img width="1920" height="1080" alt="Login Page<img width="1920" height="1080" alt="Options" src="https://github.com/user-attachments/assets/f7e6c80d-9452-4131-a3ca-28fc4e3500aa" />
<img width="1920" height="1080" alt="Home Page" src="https://github.com/user-attachments/assets/fcee9c9d-f737-49d3-bfaa-922137d66c84" />
" src="https://github.com/user-attachments/assets/9dffa3f8-0cbb-48c3-b62d-815da0d30e20" />
# 🚀 Hotel Website Deployment using Terraform & Ansible

This project demonstrates automated deployment of a PHP-based hotel website on AWS using Terraform and Ansible.

Terraform provisions the AWS EC2 infrastructure, while Ansible automatically installs Apache Web Server, MySQL Database Server, and deploys the PHP hotel website application.

---

# 📌 Project Overview

This project automates the complete deployment workflow:

1. Terraform launches AWS EC2 instance
2. Terraform triggers Ansible playbook
3. Ansible installs Apache Web Server
4. Ansible installs MySQL Database Server
5. PHP hotel website code is deployed automatically
6. Application becomes publicly accessible

---

# 🏗️ Architecture Diagram

```text
                    ┌────────────────────┐
                    │     Terraform      │
                    │────────────────────│
                    │ Launch AWS EC2     │
                    └─────────┬──────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │        Ansible         │
                 │────────────────────────│
                 │ Install Apache         │
                 │ Install MySQL          │
                 │ Deploy PHP Code        │
                 └─────────┬──────────────┘
                           │
        ┌──────────────────┼──────────────────┐
        ▼                  ▼                  ▼
┌──────────────┐  ┌────────────────┐  ┌────────────────┐
│ Apache       │  │ MySQL Server   │  │ PHP Hotel App  │
│ Web Server   │  │ Database       │  │ Website        │
└──────────────┘  └────────────────┘  └────────────────┘
                           │
                           ▼
                 ┌────────────────────────┐
                 │   Hotel Website Live   │
                 └────────────────────────┘
```

---

# ⚙️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Terraform | Infrastructure Provisioning |
| AWS EC2 | Cloud Hosting |
| Ansible | Configuration Management |
| Apache | Web Server |
| MySQL | Database Server |
| PHP | Web Application |
| Linux | Server Environment |

---

# 🚀 Deployment Flow

```text
Terraform Launches AWS EC2
              │
              ▼
Ansible Connects to Server
              │
              ├── Install Apache Web Server
              ├── Install MySQL Database
              ├── Configure Services
              └── Deploy PHP Website
              │
              ▼
Hotel Website Live on Public IP
```

---

# ☁️ Infrastructure Deployment

## Configure Terraform Variables

Update the `terraform.tfvars` file with your AWS credentials.

```bash
% cat terraform.tfvars

AWS_ACCESS_KEY=""
AWS_SECRET_KEY=""
AWS_REGION="us-east-1"
```

## Initialize Terraform

```bash
terraform init
```

## Apply Infrastructure

```bash
terraform apply --auto-approve
```

## Destroy Infrastructure

```bash
terraform destroy --auto-approve
```

---

## 🌐 Application Access

After successful deployment, access the hotel website:

```text
http://<EC2-PUBLIC-IP>
```

---

## 🔐 EC2 Server Access

```bash
ssh -i ~/.ssh/id_rsa ubuntu@<EC2-PUBLIC-IP>
```

---

## 🛢️ MySQL Credentials

```bash
mysql -uhotel_user -ppassword123
```

---

## 📤 Terraform Output Example

```text
App-Live:
PHP Application Live: http://<EC2-PUBLIC-IP>

EC2-Instance-access-details:
ssh -i ~/.ssh/id_rsa ubuntu@<EC2-PUBLIC-IP>

MYSQL-Credentials:
mysql -uhotel_user -ppassword123
```

---
