# Shopify Trigger

The **Shopify Trigger** starts an orchestration when a specified event occurs in your Shopify store — such as an order being created, a cart updated, or a product changed.

![Shopify Trigger Node](/images/agentverse/shopify-trigger-node.png)

---

## Use Cases

- Trigger an order fulfillment workflow when a new order is placed
- Notify a Slack channel when a customer abandons their cart
- Sync product changes to an external system when a product is updated
- Run post-purchase AI workflows when checkout completes

---

## Credentials

This node requires a **Shopify** credential.

To create a credential:
1. Go to **Settings → Credentials → New Credential**
2. Select **Shopify**
3. Enter your Shopify store URL and API access token

---

## Node Reference

### Parameters

| Parameter | Type | Description |
|---|---|---|
| **Credential** | Credential | Select or create a Shopify credential |
| **Trigger On** | Select | The Shopify event that starts the orchestration (see below) |

### Webhook URL

The Shopify Trigger displays a unique **Webhook URL** in the node panel. Register this URL in your Shopify app's **Webhooks** settings (Admin → Settings → Notifications → Webhooks).

### Event Types

| Event | Description |
|---|---|
| `App Uninstalled` | The Shopify app is uninstalled from the store |
| `Cart Created` | A new shopping cart is created |
| `Cart Updated` | Items in a cart are added, removed, or changed |
| `Checkout Created` | A checkout session is initiated |
| `Checkout Delete` | A checkout session is deleted |
| `Checkout Update` | A checkout session is updated |
| `Collection Created` | A new product collection is created |
| `Collection Deleted` | A product collection is deleted |
| `Collection Updated` | A product collection is updated |
| `Customer Created` | A new customer account is created |
| `Customer Deleted` | A customer account is deleted |
| `Customer Updated` | A customer account is updated |
| `Draft Order Created` | A new draft order is created |
| `Draft Order Deleted` | A draft order is deleted |
| `Draft Order Updated` | A draft order is updated |
| `Fulfillment Created` | An order fulfillment is created |
| `Fulfillment Updated` | An order fulfillment status changes |
| `Order Cancelled` | An order is cancelled |
| `Order Created` | A new order is placed |
| `Order Fulfilled` | An order is fully fulfilled |
| `Order Paid` | An order payment is confirmed |
| `Order Updated` | An order is updated |
| `Product Created` | A new product is created |
| `Product Deleted` | A product is deleted |
| `Product Updated` | A product is updated |
| `Refund Created` | A refund is issued on an order |

---

## Output Data

The trigger outputs the full Shopify webhook payload for the event. For an `Order Created` event:

```json
{
  "id": 5678901234,
  "name": "#1001",
  "email": "customer@example.com",
  "total_price": "99.00",
  "currency": "USD",
  "financial_status": "paid",
  "line_items": [
    {
      "title": "Blue T-Shirt",
      "quantity": 2,
      "price": "49.50"
    }
  ],
  "created_at": "2025-03-10T09:00:00-05:00"
}
```

Reference fields in downstream nodes:

```
{{ shopifyTrigger.name }}
{{ shopifyTrigger.email }}
{{ shopifyTrigger.total_price }}
{{ shopifyTrigger.line_items[0].title }}
```

---

## Related Nodes

- [Shopify](./shopify.md) — Read and update Shopify data within an orchestration
- [Slack](./slack.md) — Send a notification when an order event occurs
- [AI Agent](./ai-agent.md) — Process order data with an LLM
