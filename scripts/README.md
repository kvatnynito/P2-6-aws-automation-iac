# Scripts

This directory will store scripts for the AWS Automation & Infrastructure as Code project.

## Planned Script Categories

- Bash scripts
- Python scripts
- AWS CLI helper workflows
- Cleanup checks
- Security validation checks

## Script Safety Rules

Scripts must not expose or commit secrets.

Do not include:

- AWS access keys
- Secret access keys
- Session tokens
- Private SSH keys
- `.env` files
- Credential files
- Hardcoded account-specific secrets

## Destructive Actions

Scripts that delete, terminate, or modify resources must require clear confirmation.

The first version of automation should focus on review and validation before making changes.
