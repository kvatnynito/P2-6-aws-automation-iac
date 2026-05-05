# Terraform Infrastructure as Code Plan

## Status

Planned.

This document will define the planned Terraform approach for the AWS automation and Infrastructure as Code lab.

---

## Purpose

The purpose of this document is to introduce Terraform as a repeatable way to define AWS infrastructure.

Terraform should be used carefully, with cost control and cleanup as part of the workflow.

---

## Planned Terraform Learning Goals

This lab should develop basic understanding of:

- Terraform providers
- Resources
- Variables
- Outputs
- State
- `terraform init`
- `terraform fmt`
- `terraform validate`
- `terraform plan`
- `terraform apply`
- `terraform destroy`

---

## Planned Terraform Scope

Initial Terraform should stay simple.

Possible resources:

| Resource | Planned Use |
|---|---|
| VPC | Optional starter resource |
| Subnet | Optional starter resource |
| Security group | Good beginner IaC target |
| S3 bucket | Good beginner IaC target |
| EC2 instance | Optional, only if cost-controlled |

---

## Terraform Files to Create Later

Potential structure:

    terraform/
    ├── README.md
    ├── main.tf
    ├── variables.tf
    ├── outputs.tf
    ├── providers.tf
    └── .gitignore

---

## Terraform State Warning

Terraform state may contain sensitive information.

Do not commit:

- `terraform.tfstate`
- `terraform.tfstate.backup`
- `.terraform/`
- `.terraform.lock.hcl` decision to be reviewed later
- Variable files containing secrets
- Plan files containing sensitive values

---

## Planned `.gitignore` Items

Later Terraform work should include a `.gitignore` that excludes:

    .terraform/
    terraform.tfstate
    terraform.tfstate.backup
    *.tfvars
    *.tfplan
    crash.log

---

## Terraform Workflow

Planned workflow:

1. Write Terraform files.
2. Run `terraform fmt`.
3. Run `terraform validate`.
4. Run `terraform plan`.
5. Review planned resources.
6. Run `terraform apply` only when ready.
7. Validate resources in AWS.
8. Run `terraform destroy` when complete.
9. Confirm resources are removed.
10. Check billing dashboard.

---

## Cost-Control Rules

Terraform can create resources quickly.

Rules:

- Start with low-cost resources
- Avoid NAT Gateway
- Avoid load balancers
- Avoid large EC2 instances
- Use short test windows
- Always destroy test resources
- Confirm cleanup manually

---

## Planned Evidence

Later implementation may include:

- Terraform file examples
- `terraform plan` output
- `terraform apply` notes
- `terraform destroy` validation
- Lessons learned
