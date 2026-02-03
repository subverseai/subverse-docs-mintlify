---
title: HTTP Header Auth Credentials
description: How to create and configure HTTP Header authentication credentials for SubverseAI
---

# HTTP Header Auth Credentials

HTTP Header Auth credentials allow your SubverseAI agents to authenticate with web services using custom HTTP headers for API access.

## Overview

HTTP Header Auth provides access to:
- Custom header-based authentication
- API key authentication in headers
- Service-specific authentication schemes
- Legacy system integration
- Flexible authentication methods

## Dashboard Screenshot

![API Service Dashboard](https://example.com/screenshots/header-auth-dashboard.png)
*Configure header authentication in your service provider's dashboard*

## Steps to Create HTTP Header Auth Credentials

### 1. Identify Header Auth Requirements
Check your API documentation to determine the required header format:
- Look for custom header authentication
- Check for API key in headers
- Verify header name and value format
- Note any required prefixes or formats

### 2. Get Header Authentication Details
From your service provider, collect:
- **Header Name**: The custom header name (e.g., "X-API-Key")
- **Header Value**: The authentication value or API key
- **Prefix** (optional): Any required prefix (e.g., "Bearer ", "Token ")
- **Additional Headers** (optional): Any other required headers

### 3. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **HTTP Header Auth** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Header Name**: Your custom header name
   - **Header Value**: Your authentication value or API key
   - **Prefix** (optional): Required prefix for the header value
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Header Name**: Your custom header name
- **Header Value**: Your authentication value or API key
- **Prefix** (optional): Required prefix for the header value

## Usage Tips

- Use HTTPS endpoints to protect headers in transit
- Follow the exact header format specified in API documentation
- Store API keys securely and rotate regularly
- Use environment-specific credentials for different stages

## Troubleshooting

**401 Unauthorized**: Verify header name and value are correct

**Missing Header**: Ensure the header name matches API requirements exactly

**Invalid Format**: Check for required prefixes or formatting

**Case Sensitivity**: Header names are case-insensitive but values may be case-sensitive

## Next Steps

After creating your HTTP Header Auth credentials:
- Set up custom header-based API integrations
- Configure service-specific authentication workflows
- Build legacy system connections
- Test different header formats and values
- Monitor authentication success and failure rates
