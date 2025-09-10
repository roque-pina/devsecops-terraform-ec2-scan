# DevSecOps Project: Terraform EC2 + Trivy/Checkov Scan

This project demonstrates how to create an EC2 instance using Terraform and scan the infrastructure code using Trivy and/or Checkov via GitHub Actions.

## ✅ What It Does
- Provisions an EC2 instance in AWS using Terraform
- Uses GitHub Actions to run security scans on the Terraform code
- Flags misconfigurations before deployment

## 🧪 Tools Used
- Terraform
- Trivy or Checkov (choose your scanner)
- GitHub Actions
- AWS (IAM/EC2)

## 🚀 How to Use
1. Clone this repo
2. Review and customize the Terraform code under `iac/`
3. Push to GitHub – the workflow will run automatically

## 🛡️ Security Checks
- IAM policy misuse
- Public S3 buckets (if any)
- Open security groups
- Deprecated instance types