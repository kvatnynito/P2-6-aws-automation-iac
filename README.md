# P2-6: AWS Automation & Infrastructure as Code

## Overview

This repository is part of **Cybersecurity Portfolio 2: AWS Cloud Security & Engineering**.

The purpose of this project is to design and document AWS automation and Infrastructure as Code workflows. This lab will focus on AWS CLI usage, Bash scripting, Python/boto3 automation, Terraform basics, security validation checks, and resource cleanup automation.

This project is planned as the sixth AWS-focused lab in Portfolio 2 because automation should build on the earlier AWS account, VPC, logging, storage, and EC2 security projects.

---

## Status

**Planned**

This project has not been implemented yet.

Work on this repository will begin after the required Portfolio 1 homelab foundation is completed and after the earlier AWS Portfolio 2 labs are prepared.

Current status:

- [ ] Automation design plan created
- [ ] AWS CLI workflows documented
- [ ] Bash automation plan created
- [ ] Python/boto3 plan created
- [ ] Terraform IaC plan created
- [ ] Security validation checks planned
- [ ] Cleanup automation plan created
- [ ] Cost-control notes created
- [ ] Screenshots and evidence collected
- [ ] Final documentation completed

---

## Portfolio Context

### Portfolio 1 Foundation

Portfolio 1 focuses on building a local cybersecurity homelab using Proxmox, pfSense, network segmentation, Active Directory, Splunk, and vulnerable systems.

Portfolio 1 builds the local infrastructure and security foundation.

### Portfolio 2 Direction

Portfolio 2 expands local infrastructure and security concepts into AWS cloud security and cloud engineering.

This repository focuses on automating AWS tasks and introducing Infrastructure as Code practices.

---

## Project Goal

The goal of this project is to understand how AWS infrastructure and security checks can be automated using CLI tools, scripts, and Infrastructure as Code.

By the end of this project, the planned AWS environment should include documentation for:

- AWS CLI workflows
- Bash automation examples
- Python/boto3 automation examples
- Terraform starter templates
- Security validation checks
- Resource cleanup automation
- Cost-control considerations
- Redacted evidence and screenshots

---

## Planned Skills

This project is intended to develop hands-on familiarity with:

- AWS CLI
- Bash scripting
- Python scripting
- boto3 basics
- Terraform basics
- Infrastructure as Code
- Cloud resource automation
- Security validation automation
- Cleanup scripting
- Repeatable deployment workflows
- Cost-conscious automation
- Technical documentation

---

## Planned Tools and Services

The following tools, AWS services, and features may be used in this project:

| Tool / Service | Planned Use |
|---|---|
| AWS CLI | Query and manage AWS resources |
| Bash | Automate simple AWS tasks and cleanup |
| Python | Build basic automation scripts |
| boto3 | Interact with AWS services using Python |
| Terraform | Define AWS infrastructure as code |
| IAM | Control permissions for automation |
| Amazon VPC | Potential IaC deployment target |
| Amazon EC2 | Potential IaC deployment target |
| Amazon S3 | Potential automation and validation target |
| CloudTrail | Review automation activity |
| CloudWatch | Optional monitoring validation |

---

## Planned Lab Sections

### 1. AWS CLI Workflows

Planned tasks:

- Configure AWS CLI safely
- Validate caller identity
- List basic AWS resources
- Query IAM, S3, EC2, and VPC resources
- Document useful commands
- Avoid exposing credentials

Expected outcome:

> AWS CLI is understood as a command-line interface for managing and validating AWS resources.

---

### 2. Bash Automation

Planned tasks:

- Create simple Bash scripts for resource review
- Automate basic inventory collection
- Automate cleanup checks
- Add comments and safe execution notes
- Avoid destructive commands without confirmation

Expected outcome:

> Bash scripts are used to automate repeatable AWS review tasks.

---

### 3. Python and boto3 Automation

Planned tasks:

- Review boto3 basics
- Write simple scripts to list AWS resources
- Query S3 bucket settings
- Query EC2 instances
- Query security groups
- Format findings for documentation

Expected outcome:

> Python and boto3 are used to automate AWS security and inventory checks.

---

### 4. Terraform Infrastructure as Code

Planned tasks:

- Review Terraform basics
- Create starter Terraform structure
- Plan simple AWS resources
- Document `terraform init`, `plan`, `apply`, and `destroy`
- Avoid deploying complex or expensive resources
- Use variables and outputs safely

Expected outcome:

> Terraform is introduced as a repeatable method for defining AWS infrastructure.

---

### 5. Security Validation Checks

Planned tasks:

- Plan checks for public S3 exposure
- Plan checks for broad security group rules
- Plan checks for running EC2 instances
- Plan checks for missing tags
- Plan checks for cleanup readiness
- Document findings

Expected outcome:

> Automation is used to support security review, not just resource deployment.

---

### 6. Cleanup Automation

Planned tasks:

- Create safe cleanup checklist
- Plan scripts that identify resources to remove
- Avoid automatic deletion without review
- Document cleanup commands
- Confirm resources are removed after testing

Expected outcome:

> Resource cleanup becomes part of the automation workflow to reduce cost and risk.

---

## Planned Deliverables

This repository is expected to include:

- Automation design plan
- AWS CLI workflow documentation
- Bash script plan
- Python/boto3 script plan
- Terraform starter plan
- Security validation check documentation
- Cleanup automation plan
- Example scripts
- Terraform starter files
- Cost-control notes
- Redacted screenshots
- Lessons learned
- Final project summary

---

## Proposed Repository Structure

    P2-6-aws-automation-iac/
    ├── README.md
    ├── docs/
    │   ├── automation-design-plan.md
    │   ├── aws-cli-workflows.md
    │   ├── bash-automation-plan.md
    │   ├── python-boto3-plan.md
    │   ├── terraform-iac-plan.md
    │   ├── security-validation-checks.md
    │   ├── cleanup-automation-plan.md
    │   ├── cost-control-notes.md
    │   └── lessons-learned.md
    ├── scripts/
    │   ├── README.md
    │   ├── bash/
    │   │   └── README.md
    │   └── python/
    │       └── README.md
    ├── terraform/
    │   └── README.md
    ├── diagrams/
    │   └── README.md
    └── screenshots/
        └── README.md

---

## Security Notes

Sensitive information will not be committed to this repository.

This includes:

- AWS account ID
- Access keys
- Secret access keys
- Session tokens
- Private SSH keys
- Terraform state files containing sensitive data
- `.env` files
- AWS credentials files
- Unredacted ARNs
- Unredacted screenshots
- Any credential material

Automation must be designed carefully because scripts can quickly create, modify, or delete cloud resources.

---

## Cost-Control Notes

This project is designed to stay within the AWS Free Tier or near-free usage.

Special care will be taken with:

- Terraform-created resources
- EC2 instances
- EBS volumes
- EBS snapshots
- Elastic IP addresses
- NAT Gateway
- Load balancers
- CloudWatch logs
- S3 storage
- Accidentally repeated script execution

The goal is to learn automation safely without creating unnecessary cost.

---

## Relationship to AWS Solutions Architect Associate

This project supports foundational knowledge for the **AWS Certified Solutions Architect – Associate** certification by focusing on:

- Infrastructure deployment concepts
- Resource configuration
- IAM permissions
- Networking resources
- Compute resources
- Storage resources
- Monitoring validation
- Cost-aware architecture

This repository is not a certification study guide. It is a hands-on portfolio project designed to support practical AWS learning.

---

## Resume Skill Alignment

This project is intended to support resume experience related to:

- AWS CLI
- Python/boto3 automation
- Bash scripting
- Terraform basics
- Infrastructure as Code
- Cloud security validation
- Resource inventory automation
- Cleanup automation
- Cloud engineering documentation

Example resume bullet after completion:

> Automated AWS resource inventory, security validation, and cleanup workflows using AWS CLI, Bash, Python/boto3, and Terraform to support repeatable cloud security and engineering practices.

---

## Current Status Summary

This repository is currently in the planning stage.

Implementation will begin after the required Portfolio 1 foundation is completed and after the earlier AWS Portfolio 2 labs are prepared.
