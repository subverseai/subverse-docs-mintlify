---
title: S3 Storage Credentials
description: How to create and configure AWS S3 storage credentials for SubverseAI
---

# S3 Storage Credentials

S3 credentials allow your SubverseAI agents to store and retrieve files from Amazon S3 and S3-compatible storage services.

## Overview

S3 credentials provide access to:
- File storage and retrieval
- Bucket management operations
- Object upload/download
- S3-compatible storage services
- Cloud file management workflows

## Dashboard Screenshot

![AWS Console](https://example.com/screenshots/aws-s3-dashboard.png)
*Create IAM credentials in the [AWS Console](https://console.aws.amazon.com/iam/)*

## Steps to Create S3 Credentials

### 1. Create AWS Account
1. Visit [AWS Console](https://console.aws.amazon.com)
2. Sign up or sign in to your AWS account
3. Navigate to the IAM service

### 2. Create IAM Policy
1. Go to **Policies** in IAM
2. Click **Create policy**
3. Select **JSON** tab and paste:
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:GetObject",
                "s3:PutObject",
                "s3:DeleteObject",
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::your-bucket-name",
                "arn:aws:s3:::your-bucket-name/*"
            ]
        }
    ]
}
```
4. Replace `your-bucket-name` with your actual bucket name
5. Click **Next**, give the policy a name (e.g., "SubverseAI-S3-Access")
6. Click **Create policy**

### 3. Create IAM User
1. Go to **Users** in IAM
2. Click **Create user**
3. Enter a username (e.g., "subverseai-s3-user")
4. Select **Access key - Programmatic access**
5. Click **Next**
6. Attach the policy you created in step 2
7. Click **Next**, **Create user**

### 4. Get Access Keys
1. Copy the **Access key ID** and **Secret access key**
2. Store these securely - you won't see the secret key again

### 5. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **S3 Storage** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Access Key ID**: Your AWS access key
   - **Secret Access Key**: Your AWS secret key
   - **Region**: AWS region (e.g., `us-east-1`)
   - **Bucket Name**: Your S3 bucket name
   - **Endpoint** (optional): For S3-compatible services
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Access Key ID**: Your AWS access key ID
- **Secret Access Key**: Your AWS secret access key
- **Region**: AWS region for your bucket
- **Bucket Name**: Your S3 bucket name
- **Endpoint** (optional): Custom endpoint for S3-compatible services

## Usage Tips

- Use IAM users instead of root account credentials
- Grant minimum required permissions only
- Use different buckets for different environments
- Enable S3 versioning for important data
- Configure bucket policies for additional security

## Troubleshooting

**Access Denied**: Check IAM permissions and bucket policies

**Invalid Credentials**: Verify access key and secret key are correct

**Bucket Not Found**: Ensure bucket name is correct and in the right region

**Endpoint Error**: For non-AWS S3 services, configure the custom endpoint

## Next Steps

After creating your S3 credentials:
- Set up file upload/download workflows
- Configure automated backups
- Build file processing pipelines
- Integrate with other cloud storage services
- Monitor storage usage and costs
