# Webhook Trigger

The **Webhook** trigger starts an orchestration when an HTTP request is received at a unique URL generated for that orchestration.

![Webhook Trigger Node](/images/agentverse/webhook-trigger-node.png)

---

## Use Cases

- Receive data from third-party services (GitHub, Stripe, Typeform, etc.)
- Build custom HTTP endpoints without infrastructure setup
- Handle form submissions or API integrations

---

## Node Reference

### Parameters

| Parameter | Type | Description |
|---|---|---|
| **Allow Multiple HTTP Methods** | Boolean | When enabled, the webhook accepts requests from more than one HTTP method |
| **Respond** | Select | When and how to respond to the caller (see below) |

### Respond Options

| Option | Description |
|---|---|
| `Immediately` | Responds as soon as the request is received, before the orchestration finishes |
| `When Last Node Finishes` | Waits for the full orchestration to complete, then responds with the last node's output |
| `Using Respond to Webhook Node` | Defers the response to an explicit [Respond to Webhook](./respond-to-webhook.md) node placed later in the orchestration |

### Options

| Option | Description |
|---|---|
| **Response Code** | The HTTP status code to return (default: `200`) |
| **Response Headers** | Custom headers to include in the response |
| **IP(s) Whitelist** | Comma-separated list of allowed IP addresses or CIDR ranges. Leave empty to allow all. |

---

## Webhook URL

Each orchestration gets a unique webhook URL shown inside the node. Copy it using the **Copy URL** link.

> The production URL is only active when the orchestration is **Activated**. A separate test URL is available while editing.

---

## Output Data

The Webhook trigger outputs an object with the full HTTP request details:

```json
{
  "headers": {
    "content-type": "application/json",
    "authorization": "Bearer ..."
  },
  "params": {},
  "query": {
    "source": "stripe"
  },
  "body": {
    "event": "payment.completed",
    "amount": 4999
  },
  "webhookUrl": "https://...",
  "executionMode": "production"
}
```

Reference fields in downstream nodes:

```
{{ webhook.body.event }}
{{ webhook.query.source }}
{{ webhook.headers.authorization }}
```

---

## Related Nodes

- [Respond to Webhook](./respond-to-webhook.md) — Send a custom HTTP response back to the caller
- [Schedule Trigger](./schedule-trigger.md) — Trigger on a time-based schedule instead
