# Python boto3 Plan

## Status

Planned.

This document will define planned Python and boto3 automation ideas for AWS security and inventory checks.

---

## Purpose

The purpose of this document is to plan Python scripts that use boto3 to query AWS resources and support security review.

Python will be used where structured logic is more useful than simple shell commands.

---

## Planned Python Script Ideas

| Script Idea | Purpose |
|---|---|
| list_s3_buckets.py | List S3 buckets |
| check_s3_public_access.py | Review S3 public access settings |
| list_ec2_instances.py | List EC2 instance status |
| review_security_groups.py | Identify broad inbound rules |
| cloudtrail_lookup.py | Review recent CloudTrail events |
| cleanup_inventory.py | List resources that may need cleanup |

---

## boto3 Concepts to Learn

| Concept | Purpose |
|---|---|
| Session | Manage AWS profile and region context |
| Client | Low-level service interaction |
| Resource | Higher-level object-oriented interaction |
| Pagination | Handle large result sets |
| Exceptions | Handle AWS API errors |
| JSON output | Format results clearly |

---

## Python Safety Rules

Scripts should:

- Avoid hardcoded credentials
- Use AWS profiles or environment configuration safely
- Redact sensitive output when needed
- Handle errors cleanly
- Avoid destructive actions by default
- Print clear results
- Include comments explaining logic

---

## Example Output Goals

Script output should be easy to understand.

Example categories:

- Resource name
- Region
- Status
- Risk indicator
- Recommended review action

---

## Security Checks to Build Later

Potential checks:

- S3 bucket public access status
- Security groups allowing `0.0.0.0/0` to sensitive ports
- Running EC2 instances
- Unused security groups
- Missing tags
- CloudTrail status
- GuardDuty status

---

## Planned Evidence

Later implementation may include:

- Python scripts
- Redacted script output
- Error handling examples
- Findings table
- Lessons learned
