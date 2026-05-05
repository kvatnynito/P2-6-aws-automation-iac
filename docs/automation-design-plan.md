# Automation Design Plan

## Status

Planned.

This document will define the planned AWS automation strategy for this lab.

---

## Purpose

The purpose of this document is to plan how automation will be used to support AWS cloud security and engineering workflows.

Automation should make tasks repeatable, documented, safer, and easier to validate.

---

## Automation Goals

This lab should use automation to support:

- AWS resource inventory
- Security configuration review
- Repeatable infrastructure deployment
- Cleanup validation
- Cost-control checks
- Documentation support
- Reduced manual error

---

## Planned Automation Areas

| Area | Planned Tool |
|---|---|
| Resource inventory | AWS CLI / Python |
| S3 security checks | AWS CLI / Python |
| Security group review | AWS CLI / Python |
| EC2 instance review | AWS CLI / Python |
| Cleanup checks | Bash / Python |
| Infrastructure deployment | Terraform |
| Validation commands | AWS CLI |

---

## Automation Principles

Planned principles:

1. Start simple.
2. Avoid destructive automation at first.
3. Require confirmation before deletion.
4. Log or print what the script is doing.
5. Do not hardcode credentials.
6. Do not commit secrets.
7. Keep scripts readable.
8. Document expected inputs and outputs.
9. Test against small lab resources.
10. Clean up resources after testing.

---

## Risk Considerations

| Risk | Mitigation |
|---|---|
| Script deletes wrong resource | Require manual confirmation |
| Credentials exposed | Use AWS CLI profiles and environment controls safely |
| Terraform state contains sensitive data | Do not commit state files |
| Infinite or repeated resource creation | Use small tests and review plans |
| Unexpected cost | Use budgets and cleanup scripts |
| Overly broad IAM permissions | Use least privilege where possible |

---

## Planned Evidence

Later implementation may include:

- Script output screenshots
- Command examples
- Terraform plan output
- Cleanup validation notes
- Security check findings
- Lessons learned
