# Cost-Control Notes

## Status

Planned.

This document will track cost-control considerations for the AWS Automation & Infrastructure as Code lab.

---

## Purpose

The purpose of this document is to prevent unnecessary AWS costs while testing automation and Infrastructure as Code.

Automation can create resources quickly, which means mistakes can become expensive quickly.

---

## Services and Features to Watch

| Service / Feature | Cost Risk |
|---|---|
| EC2 instances | Can run continuously if not stopped |
| EBS volumes | Can remain after instance deletion |
| EBS snapshots | Can accumulate storage charges |
| Elastic IP addresses | Can create charges if unused |
| NAT Gateway | Can create hourly and data-processing charges |
| Load balancers | Can create ongoing charges |
| CloudWatch logs | Log ingestion and retention can create charges |
| S3 buckets | Storage and requests can create cost |
| Terraform-created resources | May persist if not destroyed |
| Repeated script execution | Can create duplicate resources |

---

## Cost-Control Rules

Planned rules:

1. Configure billing alerts before implementation.
2. Use one AWS region.
3. Start with read-only automation.
4. Avoid destructive or resource-creating scripts until reviewed.
5. Avoid NAT Gateway in beginner Terraform builds.
6. Avoid load balancers in this repo.
7. Use Free Tier eligible resources where possible.
8. Run `terraform plan` before `terraform apply`.
9. Run `terraform destroy` after temporary tests.
10. Check billing dashboard after automation testing.

---

## Automation Safety Controls

Scripts should include:

- Clear purpose statement
- Region awareness
- Caller identity check
- Dry-run mode where possible
- Confirmation before deletion
- Error handling
- Clear output
- No hardcoded secrets

---

## Terraform Cleanup Checklist

After Terraform testing:

- [ ] Run `terraform destroy`
- [ ] Confirm destroy completed successfully
- [ ] Check AWS console for remaining resources
- [ ] Review EC2 instances
- [ ] Review EBS volumes
- [ ] Review Elastic IPs
- [ ] Review S3 buckets
- [ ] Review security groups
- [ ] Check billing dashboard
- [ ] Document cleanup result

---

## Evidence to Collect Later

Later implementation may include:

- Redacted billing screenshot
- Terraform destroy output
- Cleanup script output
- Cost lessons learned
