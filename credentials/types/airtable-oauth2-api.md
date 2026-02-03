---
title: Airtable OAuth2 API Credentials
description: How to create and configure Airtable OAuth2 API credentials for SubverseAI
---

# Airtable OAuth2 API Credentials

Airtable OAuth2 API credentials allow your SubverseAI agents to authenticate with Airtable using the OAuth2 standard for secure API access.

## Overview

Airtable OAuth2 credentials provide access to:
- OAuth2-based Airtable API authentication
- Automatic token refresh
- Secure user-specific access
- Enterprise integration
- Enhanced security workflows

## Dashboard Screenshot

![Airtable Developer Hub](https://example.com/screenshots/airtable-oauth2-dashboard.png)
*Create OAuth2 apps in the [Airtable Developer Hub](https://airtable.com/developers/web/api)*

## Steps to Create Airtable OAuth2 API Credentials

### 1. Create Airtable Account
1. Visit [Airtable](https://airtable.com)
2. Sign up or sign in to your account
3. Navigate to the **Developer Hub**

### 2. Create OAuth2 App
1. Go to **Developer Hub** > **OAuth2**
2. Click **Create new OAuth2 application**
3. Enter application details:
   - **Name**: Descriptive name (e.g., "SubverseAI OAuth2 Integration")
   - **Description**: Brief description of your integration
   - **Logo**: Upload app logo (optional)
4. Configure **Redirect URIs**:
   - Add your SubverseAI callback URL
   - Format: `https://your-subverseai-domain.com/oauth/callback`
5. Click **Create application**

### 3. Get OAuth2 Credentials
From your app settings, collect:
- **Client ID**: Your OAuth2 client identifier
- **Client Secret**: Your OAuth2 client secret
- **Authorization URL**: Airtable OAuth2 authorization endpoint
- **Token URL**: Airtable OAuth2 token endpoint

### 4. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **Airtable OAuth2 API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Client ID**: Your Airtable OAuth2 client ID
   - **Client Secret**: Your Airtable OAuth2 client secret
   - **Scope**: Required permissions (e.g., "data.records:read data.records:write")
   - **Redirect URI**: Your OAuth2 callback URL
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Client ID**: Your Airtable OAuth2 client ID
- **Client Secret**: Your Airtable OAuth2 client secret
- **Scope**: Required permissions (space-separated)
- **Redirect URI**: OAuth2 callback URL

## Usage Tips

- Use specific scopes to limit access to required operations
- Test with different workspaces and bases
- Monitor token refresh and expiration
- Use separate apps for development and production

## Troubleshooting

**Invalid Client**: Verify Client ID and Secret are correct

**Redirect URI Mismatch**: Ensure the redirect URI matches exactly

**Scope Insufficient**: Add required Airtable API scopes

**Workspace Access**: Ensure the app has access to target workspaces

## Next Steps

After creating your Airtable OAuth2 credentials:
- Set up OAuth2 authentication workflows
- Configure automatic token refresh
- Build workspace-specific integrations
- Test different base and table access
- Monitor authentication success rates
