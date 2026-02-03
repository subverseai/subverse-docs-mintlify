---
title: Shopify OAuth2 API Credentials
description: How to create and configure Shopify OAuth2 API credentials for SubverseAI
---

# Shopify OAuth2 API Credentials

Shopify OAuth2 API credentials allow your SubverseAI agents to authenticate with Shopify stores using the OAuth2 standard for secure API access.

## Overview

Shopify OAuth2 credentials provide access to:
- OAuth2-based Shopify API authentication
- Automatic token refresh
- Secure app integration
- Multi-store management
- Enhanced security workflows

## Dashboard Screenshot

![Shopify Partners Dashboard](https://example.com/screenshots/shopify-oauth2-dashboard.png)
*Create OAuth2 apps in the [Shopify Partners Dashboard](https://partners.shopify.com)*

## Steps to Create Shopify OAuth2 API Credentials

### 1. Create Shopify Partners Account
1. Visit [Shopify Partners](https://partners.shopify.com)
2. Create a Partners account or sign in
3. Navigate to **Apps** > **Create app**

### 2. Create OAuth2 App
1. Click **Create app**
2. Select **Build an app**
3. Enter app name (e.g., "SubverseAI OAuth2 Integration")
4. Select the app developer
5. Click **Create app**

### 3. Configure OAuth2 Settings
1. Go to the **Configuration** tab
2. In the **App credentials** section, note:
   - **API key** (Client ID)
   - **API secret key** (Client Secret)
3. Set the **Redirection URL** to your SubverseAI callback URL
4. Configure the required Admin API access scopes

### 4. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **Shopify OAuth2 API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Client ID**: Your Shopify app API key
   - **Client Secret**: Your Shopify app API secret
   - **Store URL**: Your Shopify store domain
   - **Scope**: Required permissions (comma-separated)
   - **Redirect URI**: OAuth2 callback URL
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Client ID**: Your Shopify app API key
- **Client Secret**: Your Shopify app API secret
- **Store URL**: Your Shopify store domain
- **Scope**: Required permissions (comma-separated)
- **Redirect URI**: OAuth2 callback URL

## Usage Tips

- Use the minimum required scopes for your use case
- Test with development stores before production
- Monitor token refresh and expiration
- Use separate apps for different environments

## Troubleshooting

**Invalid Client**: Verify Client ID and Secret are correct

**Redirect URI Mismatch**: Ensure the redirect URI matches exactly

**Scope Insufficient**: Add required Admin API scopes

**Store Not Found**: Verify the store URL is correct and accessible

## Next Steps

After creating your Shopify OAuth2 credentials:
- Set up OAuth2 authentication workflows
- Configure automatic token refresh
- Build multi-store management systems
- Test API endpoints and permissions
- Monitor authentication success rates
