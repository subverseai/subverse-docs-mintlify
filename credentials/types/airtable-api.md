---
title: Airtable API Credentials
description: How to create and configure Airtable API credentials for SubverseAI
---

# Airtable API Credentials

Airtable API credentials allow your SubverseAI agents to interact with Airtable bases for database operations and data management.

## Overview

Airtable credentials provide access to:
- Database operations (CRUD)
- Table and record management
- Data synchronization
- Spreadsheet-like database operations
- Collaborative data workflows

## Dashboard Screenshot

![Airtable Developer Hub](https://example.com/screenshots/airtable-dashboard.png)
*Create API tokens in the [Airtable Developer Hub](https://airtable.com/create/tokens)*

## Steps to Create Airtable API Credentials

### 1. Create Airtable Account
1. Visit [Airtable](https://airtable.com)
2. Sign up or sign in to your account
3. Create or select a workspace

### 2. Generate Personal Access Token
1. Navigate to the [Developer Hub](https://airtable.com/create/tokens)
2. Click **Create new token**
3. Enter a token name (e.g., "SubverseAI Integration")
4. Set permissions:
   - Select the workspaces to access
   - Choose scopes (read, create, update, delete)
5. Click **Create token**
6. Copy the token immediately - it won't be shown again

### 3. Get Base and Table IDs
1. Open your Airtable base
2. From the URL, copy the **Base ID** (the part after `https://airtable.com/`)
3. Go to **Help** > **API documentation**
4. Select your base to see table IDs
5. Note the **Table IDs** for tables you want to access

### 4. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **Airtable API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Personal Access Token**: Your Airtable API token
   - **Base ID** (optional): Default base ID for operations
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Personal Access Token**: Your Airtable personal access token
- **Base ID** (optional): Default base ID for operations

## Usage Tips

- Use specific scopes to limit token permissions
- Create separate tokens for different environments
- Regularly rotate your access tokens
- Use base and table IDs rather than names for reliability

## Troubleshooting

**Invalid Token**: Ensure you copied the complete token including the `pat` prefix

**Permission Denied**: Check that your token has the required scopes and workspace access

**Base Not Found**: Verify the Base ID is correct and you have access to that base

**Rate Limit Exceeded**: Airtable has API rate limits - implement retry logic

## Next Steps

After creating your Airtable credentials:
- Set up data synchronization workflows
- Create database automation workflows
- Build data import/export processes
- Configure real-time data updates
- Integrate with other data sources
