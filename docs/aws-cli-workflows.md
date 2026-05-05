# AWS CLI Workflows

## Status

Planned.

This document will track planned AWS CLI workflows for the automation and Infrastructure as Code lab.

---

## Purpose

The purpose of this document is to document useful AWS CLI commands for validating account identity, reviewing resources, and supporting security checks.

---

## AWS CLI Safety Notes

Do not commit:

- AWS access keys
- Secret access keys
- Session tokens
- AWS credentials file
- AWS config file with sensitive details
- Command output containing sensitive account data

---

## Planned CLI Validation Commands

### Caller Identity

    aws sts get-caller-identity

Purpose:

Confirm which AWS identity is being used before running commands.

---

### List S3 Buckets

    aws s3api list-buckets

Purpose:

Review S3 buckets in the account.

---

### List EC2 Instances

    aws ec2 describe-instances

Purpose:

Review EC2 instances and running workload status.

---

### List VPCs

    aws ec2 describe-vpcs

Purpose:

Review VPCs in the selected region.

---

### List Security Groups

    aws ec2 describe-security-groups

Purpose:

Review security groups and exposure rules.

---

### CloudTrail Event Lookup

    aws cloudtrail lookup-events

Purpose:

Review recent AWS account activity.

---

## Planned CLI Workflows

| Workflow | Purpose |
|---|---|
| Identity validation | Confirm active AWS identity before changes |
| S3 review | List buckets and review public access settings |
| EC2 review | Identify running instances |
| Security group review | Detect broad inbound access |
| VPC review | Inventory networking resources |
| CloudTrail review | Review recent account activity |

---

## Output Handling

When saving command output:

- Redact account IDs
- Redact ARNs if sensitive
- Redact public IPs if needed
- Do not save credentials
- Store outputs only if useful for documentation

---

## Lessons Learned

To be completed after implementation.
