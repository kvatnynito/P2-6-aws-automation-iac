# Bash Automation Plan

## Status

Planned.

This document will define planned Bash automation ideas for AWS resource review and cleanup support.

---

## Purpose

The purpose of this document is to plan simple Bash scripts that support repeatable AWS CLI workflows.

Bash should be used for straightforward command chaining, resource checks, and cleanup prompts.

---

## Planned Bash Script Ideas

| Script Idea | Purpose |
|---|---|
| check-identity.sh | Confirm active AWS identity |
| list-running-ec2.sh | List running EC2 instances |
| list-s3-buckets.sh | List S3 buckets |
| review-security-groups.sh | Identify broad inbound rules |
| cleanup-check.sh | Display resources that may need cleanup |

---

## Bash Safety Rules

Scripts should:

- Use readable variable names
- Print what they are checking
- Avoid automatic deletion by default
- Ask for confirmation before destructive actions
- Exit on errors where appropriate
- Avoid hardcoded credentials
- Include comments explaining each section

---

## Example Script Header Standard

Use a consistent header in Bash scripts:

    #!/usr/bin/env bash
    # Purpose: Describe what this script checks or automates.
    # Safety: This script should not expose credentials or delete resources without confirmation.

---

## Destructive Command Rule

Destructive commands should not run automatically.

Examples of destructive actions:

- Terminating EC2 instances
- Deleting S3 buckets
- Deleting EBS volumes
- Deleting snapshots
- Destroying Terraform resources

Any destructive script should require clear confirmation.

---

## Planned Evidence

Later implementation may include:

- Bash script files
- Example script output
- Redacted terminal screenshots
- Cleanup validation notes
- Lessons learned
