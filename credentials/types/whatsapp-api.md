---
title: WhatsApp API Credentials
description: How to create and configure WhatsApp API credentials for SubverseAI messaging
---

# WhatsApp API Credentials

WhatsApp API credentials allow your SubverseAI agents to send and receive WhatsApp messages through the WhatsApp Business Platform.

## Overview

WhatsApp credentials provide access to:
- Send and receive WhatsApp messages
- Manage WhatsApp Business accounts
- Interactive message templates
- Media file sharing
- Customer communication workflows

## Dashboard Screenshot

![Meta Business Suite](https://example.com/screenshots/whatsapp-dashboard.png)
*Configure WhatsApp API in [Meta Business Suite](https://business.facebook.com)*

## Steps to Create WhatsApp API Credentials

### 1. Create Meta Business Account
1. Visit [Meta Business Suite](https://business.facebook.com)
2. Create a Meta Business account
3. Verify your business information

### 2. Set Up WhatsApp Business Account
1. In Meta Business Suite, navigate to **WhatsApp**
2. Click **Get Started**
3. Register your phone number for WhatsApp Business
4. Verify your phone number

### 3. Create WhatsApp App
1. Go to **Apps** in Meta Business Suite
2. Click **Create App**
3. Select **Business** app type
4. Enter app name (e.g., "SubverseAI WhatsApp")
5. Click **Create App**

### 4. Configure WhatsApp Product
1. In your app dashboard, click **Add Products**
2. Select **WhatsApp**
3. Configure WhatsApp settings:
   - Choose your WhatsApp Business Account
   - Set up message templates
   - Configure webhook URL (optional)

### 5. Get API Credentials
1. Go to **App Settings** > **Basic**
2. Copy the **App ID**
3. Go to **WhatsApp** > **API Setup**
4. Generate or copy your **Access Token**
5. Note your **Phone Number ID**

### 6. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **WhatsApp API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Access Token**: Your WhatsApp API access token
   - **Phone Number ID**: Your WhatsApp phone number ID
   - **App ID**: Your Meta app ID
   - **Webhook Verify Token** (optional): For webhook verification
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Access Token**: Your WhatsApp API access token
- **Phone Number ID**: Your WhatsApp Business phone number ID
- **App ID**: Your Meta app ID
- **Webhook Verify Token** (optional): Token for webhook verification

## Usage Tips

- Use message templates for outbound messages to comply with WhatsApp policies
- Set up webhooks to receive incoming messages in real-time
- Monitor message quality metrics in Meta Business Suite
- Use different phone numbers for different use cases

## Troubleshooting

**Invalid Access Token**: Regenerate the access token in Meta Business Suite

**Phone Number Not Verified**: Ensure your WhatsApp Business account is properly verified

**Message Template Rejected**: Follow WhatsApp's template guidelines and policies

**Webhook Not Working**: Verify webhook URL and SSL certificate

## Next Steps

After creating your WhatsApp credentials:
- Set up message sending workflows
- Configure webhook handlers for incoming messages
- Create customer support automations
- Build notification systems
- Monitor message delivery and engagement
