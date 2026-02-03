---
title: WhatsApp Trigger API Credentials
description: How to create and configure WhatsApp Trigger API credentials for SubverseAI
---

# WhatsApp Trigger API Credentials

WhatsApp Trigger API credentials allow your SubverseAI agents to set up and manage WhatsApp message triggers and webhooks for real-time messaging workflows.

## Overview

WhatsApp Trigger credentials provide access to:
- WhatsApp webhook configuration
- Message trigger setup
- Real-time message reception
- Event-driven workflows
- Automated response systems

## Dashboard Screenshot

![Meta Business Suite](https://example.com/screenshots/whatsapp-trigger-dashboard.png)
*Configure webhooks in [Meta Business Suite](https://business.facebook.com)*

## Steps to Create WhatsApp Trigger API Credentials

### 1. Set Up WhatsApp Business Account
1. Visit [Meta Business Suite](https://business.facebook.com)
2. Create or select your WhatsApp Business account
3. Verify your business information and phone number

### 2. Create WhatsApp App
1. Go to **Apps** in Meta Business Suite
2. Click **Create App**
3. Select **Business** app type
4. Enter app name (e.g., "SubverseAI WhatsApp Triggers")
5. Click **Create App**

### 3. Configure WhatsApp Product
1. In your app dashboard, click **Add Products**
2. Select **WhatsApp**
3. Configure WhatsApp settings:
   - Choose your WhatsApp Business Account
   - Set up message templates
   - Configure webhook settings

### 4. Set Up Webhook
1. In WhatsApp settings, go to **Webhooks**
2. Click **Configure**
3. Enter your webhook URL: `https://your-subverseai-domain.com/webhooks/whatsapp`
4. Select webhook events:
   - **Messages**: Incoming messages
   - **Message Status**: Delivery and read receipts
   - **Account Updates**: Account status changes
5. Click **Verify and Save**

### 5. Get Trigger Credentials
1. Go to **App Settings** > **Basic**
2. Copy the **App ID**
3. Go to **WhatsApp** > **API Setup**
4. Copy the **Access Token**
5. Note your **Phone Number ID**
6. Copy the **Webhook Verify Token**

### 6. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **WhatsApp Trigger API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Access Token**: Your WhatsApp API access token
   - **Phone Number ID**: Your WhatsApp phone number ID
   - **App ID**: Your Meta app ID
   - **Webhook Verify Token**: Your webhook verification token
   - **Webhook URL**: Your webhook endpoint URL
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Access Token**: Your WhatsApp API access token
- **Phone Number ID**: Your WhatsApp Business phone number ID
- **App ID**: Your Meta app ID
- **Webhook Verify Token**: Token for webhook verification
- **Webhook URL**: Your webhook endpoint URL

## Usage Tips

- Use HTTPS URLs for webhooks
- Test webhook endpoints before going live
- Monitor webhook delivery and failures
- Use message templates for outbound messages
- Set up proper error handling for webhook failures

## Troubleshooting

**Webhook Verification Failed**: Ensure your webhook URL is accessible and returns the correct verification token

**Message Not Received**: Check webhook event subscriptions and phone number status

**Rate Limit Exceeded**: Monitor message sending rates and implement throttling

**Template Rejected**: Follow WhatsApp's message template guidelines

## Next Steps

After creating your WhatsApp Trigger credentials:
- Set up real-time message handling workflows
- Configure automated response systems
- Build customer support automations
- Monitor webhook performance and delivery
- Test message templates and interactive messages
