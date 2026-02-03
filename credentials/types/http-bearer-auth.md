---
title: HTTP Bearer Auth Credentials
description: How to create and configure HTTP Bearer authentication credentials for SubverseAI
---

# HTTP Bearer Auth Credentials

HTTP Bearer Auth credentials allow your SubverseAI agents to authenticate with web services using Bearer tokens for secure API access.

## Overview

HTTP Bearer Auth provides access to:
- Modern REST APIs using Bearer tokens
- OAuth2 token authentication
- JWT token authentication
- API key authentication
- Secure web service integration

## Dashboard Screenshot

![API Service Dashboard](https://example.com/screenshots/bearer-auth-dashboard.png)
*Generate bearer tokens in your service provider's dashboard*

## Steps to Create HTTP Bearer Auth Credentials

### 1. Identify Bearer Auth Requirements
Check your API documentation to confirm it uses Bearer token authentication:
- Look for "Bearer Token" or "Authorization: Bearer"
- Check for token-based authentication
- Verify the token format and source

### 2. Get Bearer Token
From your service provider, collect the bearer token:
- **OAuth2 Access Token**: From OAuth2 flow
- **JWT Token**: From authentication endpoint
- **API Key**: Formatted as Bearer token
- **Custom Token**: Provider-specific token

### 3. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **HTTP Bearer Auth** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Bearer Token**: Your bearer token
   - **Header Name**: Header name (default: "Authorization")
   - **Token Prefix**: Token prefix (default: "Bearer")
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Bearer Token**: Your bearer token
- **Header Name**: Header name (default: "Authorization")
- **Token Prefix**: Token prefix (default: "Bearer")

## Usage Tips

- Use HTTPS endpoints to protect tokens in transit
- Monitor token expiration and refresh as needed
- Store tokens securely and rotate regularly
- Use environment-specific tokens for different stages

## Troubleshooting

**401 Unauthorized**: Verify bearer token is valid and not expired

**Invalid Token Format**: Check token format and encoding

**Missing Header**: Ensure header name and prefix are correct

**Token Expired**: Refresh or obtain a new token from the provider

## Next Steps

After creating your HTTP Bearer Auth credentials:
- Set up token-based API integrations
- Configure automatic token refresh workflows
- Build secure web service connections
- Monitor token usage and expiration
- Implement token validation and renewal
