# Shopify

The **Shopify** node lets you manage your Shopify store from within an orchestration — read and update orders, products, customers, and inventory.

![Shopify Node](/images/agentverse/shopify-action-node.png)

---

## Credentials

This node requires a **Shopify** credential with API access configured in your Shopify admin.

To create a credential:
1. Go to **Settings → Credentials → New Credential**
2. Select **Shopify**
3. Enter your Shopify store URL and API access token

---

## Operations

### Order

| Operation | Description |
|---|---|
| `Get` | Retrieve a single order by ID |
| `Get Many` | List orders with optional filters |
| `Create` | Create a new draft order |
| `Update` | Update order fields or status |
| `Delete` | Delete an order |
| `Fulfill` | Fulfill an order or fulfillment |
| `Cancel` | Cancel an order |

### Product

| Operation | Description |
|---|---|
| `Get` | Retrieve a single product by ID |
| `Get Many` | List products with optional filters |
| `Create` | Create a new product |
| `Update` | Update product details, variants, or images |
| `Delete` | Delete a product |

### Customer

| Operation | Description |
|---|---|
| `Get` | Retrieve a customer by ID or email |
| `Get Many` | List customers |
| `Create` | Create a new customer |
| `Update` | Update customer details |
| `Delete` | Delete a customer |

### Inventory

| Operation | Description |
|---|---|
| `Adjust Level` | Increase or decrease inventory at a location |
| `Set Level` | Set inventory to a specific quantity |
| `Get Level` | Get current inventory level |

---

## Parameters: Get Many Orders

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Credential** | Credential | Yes | Select or create a Shopify credential |
| **Status** | Select | No | Filter by order status: `open`, `closed`, `cancelled`, `any` |
| **Financial Status** | Select | No | Filter by payment status: `paid`, `pending`, `refunded`, etc. |
| **Fulfillment Status** | Select | No | Filter by fulfillment status |
| **Created At Min** | DateTime | No | Return orders created after this time |
| **Created At Max** | DateTime | No | Return orders created before this time |
| **Limit** | Number | No | Maximum number of orders to return |

---

## Output Data

A single order from `Get Order`:

```json
{
  "id": 5678901234,
  "name": "#1001",
  "email": "customer@example.com",
  "total_price": "99.00",
  "currency": "USD",
  "financial_status": "paid",
  "fulfillment_status": null,
  "line_items": [
    {
      "id": 1234567890,
      "title": "Blue T-Shirt",
      "quantity": 2,
      "price": "49.50"
    }
  ],
  "created_at": "2025-03-10T09:00:00-05:00"
}
```

Reference fields:

```
{{ shopify.name }}
{{ shopify.email }}
{{ shopify.financial_status }}
{{ shopify.line_items[0].title }}
```

---

## Related Nodes

- [Shopify Trigger](./shopify-trigger.md) — Trigger on Shopify store events
- [Slack](./slack.md) — Notify a team channel when an order is created or updated
- [HTTP Request](./http-request.md) — Call custom Shopify API endpoints not covered by this node
