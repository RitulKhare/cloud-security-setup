# Security Setup Report

## 1. IAM Policies Implementation

- Created IAM users and groups for different roles:
  - Admin
  - Developer
  - Read-only
- Attached policies:
  - Admin: `AdministratorAccess`
  - Developer: `AmazonS3FullAccess`
  - Read-only: `AmazonS3ReadOnlyAccess`
- Enabled MFA (Multi-Factor Authentication) for all admin users
- Custom IAM policy JSON file is included in `config/iam-policy.json`

## 2. Secure Storage Configuration

- Created S3 buckets for storing sensitive data
- Enabled:
  - Block Public Access
  - Versioning for data recovery
  - Access logging to monitor usage
- Applied bucket policies for restricted access
- Bucket policy JSON file is included in `config/bucket-policy.json`

## 3. Data Encryption Setup

- Enabled server-side encryption for S3 buckets:
  - SSE-S3 (AWS-managed keys)
  - SSE-KMS (customer-managed keys)
- KMS key JSON file is included in `config/kms-key.json`
- Optional client-side encryption was considered but not implemented

## 4. Screenshots

- Include screenshots here after implementing IAM, S3, and KMS on your cloud platform.
