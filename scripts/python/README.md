# Python Scripts

This directory will store Python scripts for AWS automation using boto3.

## Planned Python Scripts

Potential scripts may include:

- `list_s3_buckets.py`
- `check_s3_public_access.py`
- `list_ec2_instances.py`
- `review_security_groups.py`
- `cloudtrail_lookup.py`
- `cleanup_inventory.py`

## Python Script Rules

Scripts should:

- Avoid hardcoded credentials
- Use boto3 sessions safely
- Handle AWS API errors
- Print clear findings
- Avoid destructive actions by default
- Redact sensitive output when needed
- Be documented well enough to explain in an interview
