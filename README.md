# 🚀 Terraform AWS S3 Infrastructure Project

## 📌 Overview

This project demonstrates how to provision AWS infrastructure using Terraform. It focuses on creating and managing an Amazon S3 bucket using Infrastructure as Code (IaC) principles, replacing manual configuration with automated deployment.

---

## 🧰 Tools & Technologies

* Terraform
* AWS (Amazon S3)
* AWS CLI

---

## 🎯 Objectives

* Understand Infrastructure as Code (IaC)
* Configure AWS provider in Terraform
* Create an S3 bucket using Terraform
* Execute Terraform lifecycle commands
* Automate infrastructure provisioning

---

## 🏗️ Architecture

Terraform → AWS Provider → S3 Bucket

---

## ⚙️ Implementation Steps

### 1️⃣ Create Terraform Configuration File

Created a `main.tf` file to define AWS provider and S3 resource.

```hcl
provider "aws" {
  region = "ap-south-1"
}

resource "aws_s3_bucket" "demo_bucket" {
  bucket = "poorva-terraform-demo"

  tags = {
    Name        = "Terraform S3 Demo"
    Environment = "Dev"
    ManagedBy = "Terraform" 
  }
}
```

---

### 2️⃣ Initialize Terraform

```bash
terraform init
```

* Downloads required provider plugins
* Prepares working directory

---

### 3️⃣ Preview Changes

```bash
terraform plan
```

* Shows execution plan before applying changes
* Helps validate configuration

---

### 4️⃣ Apply Configuration

```bash
terraform apply
```

* Provisions S3 bucket on AWS
* Requires confirmation (`yes`)

---

### 5️⃣ Destroy Infrastructure

```bash
terraform destroy
```

* Deletes created resources
* Ensures cost control and cleanup

---

## 📸 Screenshots


![terraform init](screenshots/Screenshot(137).png)
![terraform plan](screenshots/Screenshot(138).png)
![terraform apply](screenshots/Screenshot(140).png)
![s3 bucket](screenshots/Screenshot(139).png)
![terraform destroy](screenshots/Screenshot(141).png)
![terraform destroy](screenshots/Screenshot(142).png)


---

## 📚 Key Learnings

* Terraform enables infrastructure automation using code
* Lifecycle workflow: init → plan → apply → destroy
* AWS resources can be managed declaratively
* Reduces manual errors and improves consistency

---

## 🔐 Best Practices Followed

* Used Terraform for reproducible infrastructure
* Validated changes using `terraform plan`
* Cleaned up resources using `terraform destroy`
* Maintained structured and readable configuration

---

## 🧑‍💻 Author

Gajavelli Pranathi Poorva

---

## ⭐ Conclusion

This project demonstrates the practical use of Terraform to automate AWS infrastructure provisioning. It highlights the importance of Infrastructure as Code in modern DevOps workflows for scalability, consistency, and efficiency.
