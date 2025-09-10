# DevSecOps Project: Terraform EC2 + Trivy/Checkov Scan

This project demonstrates how to create an EC2 instance using Terraform and scan the infrastructure code using Trivy and/or Checkov via GitHub Actions.

## What It Does
- Provisions an EC2 instance in AWS using Terraform
- Uses GitHub Actions to run security scans on the Terraform code
- Flags misconfigurations before deployment

## Tools Used
- Terraform
- Checkov
- GitHub Actions
- AWS (EC2)

## How to Use
1. Clone this repo
2. Review and customize the Terraform code under `iac/`
3. Push to GitHub – the workflow will run automatically

## Sample Scan Result (Checkov)

When pushing this code, Checkov failed the pipeline due to security misconfigurations.

### Findings:
- **CKV_AWS_126**: Ensure that detailed monitoring is enabled for EC2 instances
- **CKV_AWS_79**: Ensure Instance Metadata Service Version 1 is not enabled
- **CKV_AWS_135**: Ensure that EC2 is EBS optimized
- **CKV_AWS_8**: Ensure all data stored in the Launch configuration or instance Elastic Blocks Store is securely encrypted
- **CKV2_AWS_41**: Ensure an IAM role is attached to EC2 instance

### What This Proves:
- The pipeline is successfully detecting and blocking insecure infrastructure
- Security checks are enforced before deployment ("shift left")
- Demonstrates real-world security validation in a CI/CD flow
