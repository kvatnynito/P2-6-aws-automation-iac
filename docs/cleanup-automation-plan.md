# Cleanup Automation Plan

## Status

Planned.

This document will define planned cleanup checks and automation for AWS lab resources.

---

## Purpose

The purpose of this document is to reduce cost and risk by identifying resources that should be stopped, deleted, or reviewed after lab sessions.

Cleanup is a core part of safe AWS homelabbing.

---

## Cleanup Goals

Cleanup workflows should help identify:

- Running EC2 instances
- Unused EBS volumes
- EBS snapshots
- Unused Elastic IP addresses
- Test S3 buckets
- CloudWatch log groups
- GuardDuty or Inspector status
- Terraform-managed resources
- Unexpected resources

---

## Cleanup Philosophy

Cleanup scripts should be careful.

Preferred approach:

1. Identify resources.
2. Print findings.
3. Ask for human review.
4. Require confirmation before deletion.
5. Validate cleanup.
6. Check billing dashboard.

---

## Planned Cleanup Checks

| Resource | Check |
|---|---|
| EC2 | List running instances |
| EBS | List available volumes |
| Snapshots | List owned snapshots |
| Elastic IP | List allocated addresses |
| S3 | List lab buckets |
| CloudWatch | List log groups |
| Security Groups | List unused groups |
| Terraform | Confirm destroy completed |

---

## Dangerous Actions

The following should not be automated without confirmation:

- Terminating EC2 instances
- Deleting EBS volumes
- Deleting snapshots
- Deleting S3 buckets
- Deleting CloudWatch log groups
- Running `terraform destroy`
- Disabling security services

---

## Cleanup Checklist

Before ending each lab session:

- [ ] Run inventory check
- [ ] Review running EC2 instances
- [ ] Review EBS volumes
- [ ] Review snapshots
- [ ] Review Elastic IPs
- [ ] Review S3 buckets
- [ ] Review CloudWatch log groups
- [ ] Review active security services
- [ ] Destroy Terraform test resources if applicable
- [ ] Confirm billing dashboard
- [ ] Document remaining resources

---

## Planned Evidence

Later implementation may include:

- Cleanup script output
- Manual cleanup checklist
- Terraform destroy output
- Billing dashboard review notes
- Lessons learned
