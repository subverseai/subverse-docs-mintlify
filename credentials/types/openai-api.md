---
title: OpenAI API Credentials
description: How to create and configure OpenAI API credentials for SubverseAI
---

# OpenAI API Credentials

OpenAI API credentials allow your SubverseAI agents to access GPT models and other OpenAI services for AI-powered workflows.

## Overview

OpenAI credentials provide access to:
- GPT-3.5, GPT-4, and GPT-4 Turbo models
- Text completion and chat completion APIs
- Embedding models for vector search
- Fine-tuning capabilities
- DALL-E image generation

## Dashboard Screenshot

![OpenAI Dashboard](https://example.com/screenshots/openai-dashboard.png)
*View your OpenAI API keys in the [OpenAI Dashboard](https://platform.openai.com/api-keys)*

## Steps to Create OpenAI API Credentials

### 1. Create OpenAI Account
1. Visit [OpenAI Platform](https://platform.openai.com)
2. Click **Sign up** and create your account
3. Verify your email address

### 2. Generate API Key
1. Navigate to the [API Keys section](https://platform.openai.com/api-keys)
2. Click **Create new secret key**
3. Give your key a descriptive name (e.g., "SubverseAI Production")
4. Copy the secret key immediately - it won't be shown again

### 3. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **OpenAI API** from the credential types
4. Enter a name for your credential (e.g., "Production OpenAI")
5. Paste your API key in the **API Key** field
6. Optionally specify an **Organization ID** if you're part of an OpenAI organization
7. Click **Test Connection** to verify the credentials work
8. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **API Key**: Your OpenAI API secret key (starts with `sk-`)
- **Organization ID** (optional): Your OpenAI organization ID

## Usage Tips

- Use different API keys for development and production environments
- Monitor your API usage in the OpenAI dashboard to avoid unexpected charges
- Consider setting usage limits in your OpenAI account settings
- Rotate your API keys regularly for security

## Troubleshooting

**Invalid API Key**: Ensure you copied the full key including the `sk-` prefix

**Rate Limit Exceeded**: Check your usage limits in the OpenAI dashboard

**Organization Required**: If you're part of an organization, make sure to include the Organization ID

## Next Steps

After creating your OpenAI credentials:
- Use them in AI workflow nodes for text generation
- Set up chat completion workflows
- Configure embedding models for vector search
- Monitor usage and costs in your SubverseAI dashboard
