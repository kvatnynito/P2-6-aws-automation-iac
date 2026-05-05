# Terraform

This directory will store Terraform files for AWS Infrastructure as Code practice.

## Status

Planned.

Terraform files have not been implemented yet.

---

## Planned Terraform Scope

Initial Terraform practice may include:

- S3 bucket
- Security group
- Simple VPC
- Simple subnet
- Optional EC2 instance only if cost-controlled

## Important Security Warning

Terraform state can contain sensitive information.

Do not commit:

- `.terraform/`
- `terraform.tfstate`
- `terraform.tfstate.backup`
- `*.tfvars`
- `*.tfplan`
- Files containing secrets

## Planned Workflow

1. Run `terraform init`.
2. Run `terraform fmt`.
3. Run `terraform validate`.
4. Run `terraform plan`.
5. Review the plan carefully.
6. Run `terraform apply` only when ready.
7. Validate resources in AWS.
8. Run `terraform destroy` after testing.
9. Confirm resources are removed.
10. Check billing dashboard.
