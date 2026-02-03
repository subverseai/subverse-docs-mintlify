---
title: Shopify API Credentials
description: How to create and configure Shopify API credentials for SubverseAI
---

# Shopify API Credentials

Shopify API credentials allow your SubverseAI agents to interact with Shopify stores for e-commerce automation and integration.

## Overview

Shopify credentials provide access to:
- Store management operations
- Product and inventory management
- Order processing and fulfillment
- Customer data management
- Analytics and reporting

## Dashboard Screenshot

![Shopify Dashboard](https://example.com/screenshots/shopify-dashboard.png)
*Create API credentials in your [Shopify Admin](https://www.shopify.com/admin)*

## Steps to Create Shopify API Credentials

### 1. Access Shopify Admin
1. Log in to your [Shopify Admin](https://www.shopify.com/admin)
2. Navigate to **Settings** > **Apps and sales channels**
3. Click **Develop apps**

### 2. Create Custom App
1. Click **Create an app**
2. Enter an app name (e.g., "SubverseAI Integration")
3. Select the app developer (your store owner)
4. Click **Create app**

### 3. Configure Admin API Access
1. Go to the **Configuration** tab
2. Click **Configure Admin API access**
3. Select the required permissions:
   - `read_products`, `write_products` for product management
   - `read_orders`, `write_orders` for order processing
   - `read_customers`, `write_customers` for customer data
   - `read_inventory`, `write_inventory` for inventory management
4. Click **Save**

### 4. Install App and Get Credentials
1. Go to the **API credentials** tab
2. Click **Install app**
3. Confirm the installation
4. Copy the **API key** and **API secret key**
5. Copy the **Access token** (generated after installation)

### 5. Add to SubverseAI
1. Go to **Credentials** in your SubverseAI dashboard
2. Click **Create New Credential**
3. Select **Shopify API** from the credential types
4. Enter a name for your credential
5. Fill in the required fields:
   - **Store URL**: Your Shopify store URL (e.g., `mystore.myshopify.com`)
   - **API Key**: Your app's API key
   - **API Secret Key**: Your app's API secret key
   - **Access Token**: The access token generated after installation
6. Click **Test Connection** to verify the credentials work
7. Click **Save Credential**

## Required Fields

- **Name**: A descriptive name for your credential
- **Store URL**: Your Shopify store domain
- **API Key**: Your Shopify app API key
- **API Secret Key**: Your Shopify app API secret
- **Access Token**: The access token for API access

## Usage Tips

- Grant only the permissions your workflows actually need
- Use different apps for development and production
- Regularly review and update app permissions
- Monitor API usage in your Shopify admin

## Troubleshooting

**Invalid Store URL**: Ensure you're using the correct `.myshopify.com` domain

**Permission Denied**: Check that your app has the required Admin API permissions

**Token Expired**: Regenerate the access token if authentication fails

## Next Steps

After creating your Shopify credentials:
- Set up product synchronization workflows
- Automate order processing and fulfillment
- Create customer management automations
- Build inventory tracking systems
