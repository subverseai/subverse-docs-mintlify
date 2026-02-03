---
title: OAuth2 API Credentials
description: How to create and configure generic OAuth2 API credentials for SubverseAI
---

# OAuth2 API Credentials

OAuth2 API credentials allow your SubverseAI agents to authenticate with any service that supports the OAuth2 standard for secure API access.

## Overview

OAuth2 credentials provide access to:
- Any OAuth2-compatible API service
- Secure token-based authentication
- Automatic token refresh
- Standardized authentication flow
- Third-party service integration

## Dashboard Screenshot

![OAuth2 Provider Dashboard](https://example.com/screenshots/oauth2-dashboard.png)
*Configure OAuth2 apps in your service provider's developer console*

## Steps to Create OAuth2 API Credentials

### 1. Identify Your OAuth2 Provider
Determine which service you want to connect to and verify it supports OAuth2:
- Google APIs
- Microsoft Graph
- Salesforce
- GitHub
- Slack
- Or any OAuth2-compatible service

### 2. Create OAuth2 App
1. Go to your service's developer console
2. Navigate to **Applications** or **API credentials**
3. Click **Create new application** or **Register app**
4. Fill in app details:
   - **App name**: Descriptive name (e.g., "SubverseAI Integration")
   - **Description**: Brief description of your integration
   - **Homepage URL**: Your SubverseAI instance URL
   - **Callback URL**: `https://your-subverseai-domain.com/oauth/callback`

### 3. Configure OAuth2 Settings
1. Select **OAuth2** as the authorization type
2. Choose the appropriate grant type (usually **Authorization Code**)
3. Set the required scopes for your use case
4. Configure redirect/callback URLs
5. Enable the application

### 4. Get OAuth2 Credentials
From your provider dashboard, collect:
- **Client ID**: Your application's client identifier
- **Client Secret**: Your application's client secret
- **Authorization URL**: OAuth2 authorization endpoint
- **Token URL**: OAuth2 token endpoint
- **Scope**: Required permissions (space-separated)

### 5. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **OAuth2 API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Client ID**: Your OAuth2 client ID
   - **Client Secret**: Your OAuth2 client secret
   - **Authorization URL**: OAuth2 authorization endpoint
   - **Token URL**: OAuth2 token endpoint
   - **Scope**: Required permissions (space-separated)
   - **Redirect URI**: Your callback URL
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Client ID**: Your OAuth2 client ID
- **Client Secret**: Your OAuth2 client secret
- **Authorization URL**: OAuth2 authorization endpoint
- **Token URL**: OAuth2 token endpoint
- **Scope**: Required permissions (space-separated)
- **Redirect URI**: OAuth2 callback URL

## Usage Tips

- Use the least privileged scopes necessary for your workflow
- Store client secrets securely and rotate them regularly
- Test with different scopes to find the minimum required permissions
- Use environment-specific apps for development and production

## Troubleshooting

**Invalid Client**: Verify client ID and secret are correct

**Redirect URI Mismatch**: Ensure the redirect URI matches exactly what's configured

**Scope Insufficient**: Add required scopes to your OAuth2 app configuration

**Token Expired**: OAuth2 tokens should refresh automatically if configured correctly

## Next Steps

After creating your OAuth2 credentials:
- Set up authentication workflows
- Configure automatic token refresh
- Build API integration workflows
- Test different API endpoints
- Monitor token usage and expiration
