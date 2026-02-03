---
title: SIP Credentials
description: How to create and configure SIP credentials for SubverseAI voice communication
---

# SIP Credentials

SIP credentials allow your SubverseAI agents to make and receive voice calls through SIP trunk providers for voice communication workflows.

## Overview

SIP credentials provide access to:
- Voice call initiation and reception
- SIP trunk integration
- VoIP telephony services
- Interactive voice response (IVR) systems
- Call routing and management

## Dashboard Screenshot

![SIP Provider Dashboard](https://example.com/screenshots/sip-dashboard.png)
*Configure SIP accounts in your VoIP provider dashboard*

## Steps to Create SIP Credentials

### 1. Choose a SIP Provider
Select a SIP trunk provider that supports your needs:
- Twilio
- Vonage
- Plivo
- Telnyx
- Or any other SIP-compatible provider

### 2. Create SIP Account
1. Sign up for an account with your chosen provider
2. Navigate to the SIP/voice section
3. Create a new SIP trunk or account
4. Configure your account settings (region, codecs, etc.)

### 3. Get SIP Credentials
From your provider dashboard, collect:
- **Username**: Your SIP account username (optional for unauthenticated trunks)
- **Password**: Your SIP account password (optional for unauthenticated trunks)
- **SIP Address**: SIP server address (required for outbound trunks, optional for inbound)

### 4. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **SIP Credentials** from the credential types
4. Enter a name for your credential
5. Fill in the fields:
   - **Username**: Your SIP username (optional for unauthenticated trunks)
   - **Password**: Your SIP password (optional for unauthenticated trunks)
   - **SIP Address**: SIP server address (required for outbound trunks, optional for inbound)
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Fields

- **Name**: A descriptive name for your credential
- **Username**: Your SIP account username (optional for unauthenticated trunks)
- **Password**: Your SIP account password (optional for unauthenticated trunks)
- **SIP Address**: SIP server address (required for outbound trunks, optional for inbound)

**Note**: All fields are optional as SIP credentials can be used for both authenticated and unauthenticated trunks depending on your use case.

## Usage Tips

- Use secure SIP (SIPS) with port 5061 for encrypted communications
- Configure firewall rules to allow SIP traffic
- Test with different codecs for optimal audio quality
- Monitor call quality and latency

## Troubleshooting

**Connection Failed**: Verify server address, port, and firewall settings

**Authentication Failed**: Double-check username and password

**Audio Issues**: Check codec compatibility and network bandwidth

**Registration Timeout**: Verify server settings and network connectivity

## Next Steps

After creating your SIP credentials:
- Set up voice call workflows
- Configure IVR systems
- Build call routing logic
- Integrate with AI agents for voice interactions
- Monitor call quality and metrics

**Note for SIP Type**: After creating SIP credentials, you'll need to configure inbound and outbound trunks to handle call routing. See the [Trunk Configuration](/integrations/telephony) documentation for next steps.
