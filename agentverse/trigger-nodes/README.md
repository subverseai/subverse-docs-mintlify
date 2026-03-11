# Trigger Nodes

Trigger nodes are the entry point of every orchestration. They listen for events — an incoming HTTP request, a schedule, a platform event — and start the orchestration when that event occurs.

Every orchestration must have exactly one trigger node. Trigger nodes have no inputs and always appear at the leftmost position on the canvas.

---

## Available Trigger Nodes

| Node | Trigger Source |
|---|---|
| [Webhook](./nodes/webhook.md) | Incoming HTTP request (POST, GET, etc.) |
| [Starter — Schedule At](./nodes/schedule-trigger.md) | Time-based schedule (cron or one-time) |
| [Starter — Manual Trigger](./nodes/manual-trigger.md) | Manual start from the AgentVerse UI |
| [Airtable Trigger](./nodes/airtable-trigger.md) | Airtable record created/updated/deleted |
| [Slack Trigger](./nodes/slack-trigger.md) | Slack message, reaction, or event |
| [WhatsApp Trigger](./nodes/whatsapp-trigger.md) | Incoming WhatsApp message |
| [Shopify Trigger](./nodes/shopify-trigger.md) | Shopify store events (orders, carts, products, etc.) |
| [SubVerse AI Trigger](./nodes/subverse-ai-trigger.md) | SubVerse AI voice call completed |

---

## Common Behavior

- Trigger nodes produce data for all downstream nodes.
- The output shape depends on the trigger type (e.g. a Webhook trigger outputs the HTTP request body).
- Orchestrations must be **activated** before trigger nodes begin listening for events.
- Manual triggers can be tested without activating the orchestration.
