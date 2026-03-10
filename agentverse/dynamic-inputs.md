---
title: 'Dynamic Inputs'
description: 'Link upstream node outputs to downstream node parameters using the {{ }} expression syntax'
---

# Dynamic Inputs

Every node in AgentVerse produces a structured JSON output when it runs. **Dynamic inputs** let you reference that output in any downstream node's parameters — turning static configuration into data-driven workflows.

<img
  style={{ borderRadius: '0.5rem' }}
  src="/images/agentverse/link-dynamic-inputs.png"
/>

---

## How It Works

When you test a node using the **Test** button, AgentVerse captures the node's real output. A **link icon** ( ⚡ ) then appears next to every parameter in downstream nodes. Clicking it opens a field picker showing all available outputs from upstream nodes — click any field to insert it as an expression.

<Steps>
  <Step title="Test the upstream node">
    Select the node whose output you want to reference. Click **Test** in the node panel. The node executes and its output is captured and displayed.
  </Step>
  <Step title="Open the downstream node">
    Click the node where you want to use the upstream data. Any parameter that supports expressions will show a **link icon** (⚡) when hovered.
  </Step>
  <Step title="Click the link icon">
    Click the ⚡ icon next to the parameter. A picker opens showing all available fields from upstream nodes, organised by node name.
  </Step>
  <Step title="Select a field">
    Browse the tree and click the field you want. AgentVerse inserts the corresponding `{{ }}` expression automatically.
  </Step>
</Steps>

<Note>
  The field picker is only populated after an upstream node has been tested. If you don't see any fields, test the upstream node first.
</Note>

---

## The `{{ }}` Expression Syntax

Expressions are written inside double curly braces: `{{ }}`. You can reference any field from any upstream node that has run.

### Basic Field Reference

```
{{ nodeName.fieldName }}
```

For example, if a **Webhook** trigger receives a POST body with a `message` field:

```
{{ webhook.body.message }}
```

### Nested Fields

Use dot notation to traverse nested objects:

```
{{ aiAgent.output.text }}
{{ shopify.order.customer.email }}
{{ airtable.fields.Status }}
```

### Array Items

Reference a specific index in an array:

```
{{ forLoop.item.name }}
{{ webhook.body.contacts[0].phone }}
```

### Multiple Expressions in One Field

Expressions can be embedded inside a string with other text:

```
Hello {{ subverseAgents.extractedData.customerName }}, your order {{ shopify.order.id }} is confirmed.
```

---

## Available Node Outputs

Each node exposes its output under its **node name** — the label shown in the canvas. If you rename a node, the expression path updates accordingly.

| Node | Example Expression |
|---|---|
| Webhook Trigger | `{{ webhook.body.message }}` |
| AI Agent | `{{ aiAgent.text }}` |
| Airtable | `{{ airtable.fields.Name }}` |
| HTTP Request | `{{ httpRequest.data.id }}` |
| SubVerse Agents | `{{ subverseAgents.extractedData.intent }}` |
| For Loop | `{{ forLoop.item }}` |
| Conditions | `{{ conditions.outputIndex }}` |

<Tip>
  Rename your nodes to descriptive names (e.g. `fetchCustomer` instead of `HTTP Request`) to make expressions easier to read and maintain.
</Tip>

---

## Testing Expressions

Before activating your orchestration, verify expressions are resolving correctly:

1. **Test each node in sequence** — start from the trigger and test nodes one by one.
2. **Check the output panel** — each tested node shows its full JSON output. Confirm the field you're referencing is present.
3. **Use the expression editor** — hover the parameter field and click ⚡ to browse and validate available fields.

<Warning>
  If an upstream node fails or is skipped, its output will not be available. Add [Conditions](./nodes/conditions.md) nodes to handle missing or null values before referencing them downstream.
</Warning>

---

## Common Patterns

### Pass webhook data to an AI prompt

```
Summarise the following customer message:
{{ webhook.body.message }}
```

### Build a dynamic Slack message from AI output

```
{{ aiAgent.text }}
```

### Reference extracted data from a SubVerse AI conversation

```
Customer intent: {{ subverseAgents.extractedData.intent }}
Preferred date: {{ subverseAgents.extractedData.preferredDate }}
```

### Use loop item data inside a loop

When iterating with a [For Loop](./nodes/for-loop.md), each iteration exposes the current item:

```
{{ forLoop.item.email }}
{{ forLoop.item.orderId }}
```

---

## Related Pages

- [Node Types](./node-types.md) — Understand all node categories and their outputs
- [Quickstart](./quickstart.md) — See dynamic inputs in action in a real orchestration
- [For Loop](./nodes/for-loop.md) — Iterating over arrays with dynamic item references
