# Security Validation Checks

## Status

Planned.

This document will define planned security checks that can be automated or semi-automated in AWS.

---

## Purpose

The purpose of this document is to identify repeatable security checks that support AWS cloud security review.

Automation should help find risky configurations faster and more consistently.

---

## Planned Checks

| Check | Tool | Purpose |
|---|---|---|
| Confirm caller identity | AWS CLI | Avoid running commands under wrong identity |
| List running EC2 instances | AWS CLI / Python | Identify active compute resources |
| Review open SSH rules | AWS CLI / Python | Detect SSH exposure |
| Review open RDP rules | AWS CLI / Python | Detect Windows admin exposure |
| Review S3 public access | AWS CLI / Python | Detect possible storage exposure |
| Review CloudTrail status | AWS CLI / Python | Confirm logging visibility |
| Review GuardDuty status | AWS CLI / Python | Confirm detection service state |
| Review untagged resources | AWS CLI / Python | Improve inventory management |

---

## High-Risk Patterns

Potential patterns to flag:

| Pattern | Why It Matters |
|---|---|
| SSH open to `0.0.0.0/0` | Exposes admin access |
| RDP open to `0.0.0.0/0` | Exposes Windows admin access |
| S3 public access not blocked | Data exposure risk |
| CloudTrail disabled | Reduced visibility |
| Unknown running EC2 instances | Cost and security risk |
| Missing tags | Harder inventory and ownership tracking |
| Unused security groups | Configuration clutter |

---

## Finding Format

Automated findings should include:

| Field | Purpose |
|---|---|
| Resource type | What was checked |
| Resource name or ID | Which resource was affected |
| Region | Where it exists |
| Finding | What risky condition was found |
| Severity | Basic priority |
| Recommendation | Suggested remediation |
| Evidence | Command output or screenshot reference |

---

## Validation Philosophy

The goal is not to build a perfect scanner.

The goal is to demonstrate practical automation that supports security review.

Good beginner automation should be:

- Clear
- Safe
- Focused
- Documented
- Repeatable
- Easy to explain in an interview

---

## Planned Evidence

Later implementation may include:

- Validation script output
- Findings table
- Remediation notes
- Before/after comparison
- Lessons learned
