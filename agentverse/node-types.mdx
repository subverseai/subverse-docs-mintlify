---
title: 'Node Types'
description: 'Overview of all AgentVerse node categories — triggers, actions, logic, and AI nodes'
---

# Node Types

AgentVerse nodes are the building blocks of every orchestration. Each node performs a specific function and connects to other nodes to form a workflow.

---

## Categories

### Trigger Nodes

Trigger nodes start an orchestration. Every orchestration must have exactly one trigger node as its entry point. Trigger nodes have no inputs — they only produce outputs.

| Node | Description |
|---|---|
| [Webhook](./nodes/webhook.md) | Start an orchestration via an incoming HTTP request |
| [Starter — Schedule At](./nodes/schedule-trigger.md) | Run an orchestration on a time-based schedule |
| [Starter — Manual Trigger](./nodes/manual-trigger.md) | Start an orchestration manually from the UI |
| [Airtable Trigger](./nodes/airtable-trigger.md) | Trigger on Airtable record events |
| [Slack Trigger](./nodes/slack-trigger.md) | Trigger on Slack events (messages, reactions, etc.) |
| [WhatsApp Trigger](./nodes/whatsapp-trigger.md) | Trigger on incoming WhatsApp messages |
| [Shopify Trigger](./nodes/shopify-trigger.md) | Trigger on Shopify store events (orders, carts, products, etc.) |
| [SubVerse AI Trigger](./nodes/subverse-ai-trigger.md) | Trigger when a SubVerse AI voice call completes |

---

### Action Nodes

Action nodes interact with external services. They receive data from upstream nodes, perform an operation (API call, database write, file upload), and return a result.

| Node | Description |
|---|---|
| [Slack](./nodes/slack.md) | Send messages, manage channels, and interact with Slack |
| [Airtable](./nodes/airtable.md) | Read, create, update, and delete Airtable records |
| [Shopify](./nodes/shopify.md) | Manage Shopify orders, products, customers, and inventory |
| [WhatsApp](./nodes/whatsapp.md) | Send WhatsApp messages and manage contacts |
| [HTTP Request](./nodes/http-request.md) | Make HTTP calls to any external API |
| [File Upload](./nodes/file-upload.md) | Upload files to cloud storage (S3) |
| [Respond to Webhook](./nodes/respond-to-webhook.md) | Send a custom HTTP response back to a webhook caller |

---

### Logic Nodes

Logic nodes control the flow of an orchestration. They branch, loop, pause, or wait for external input before continuing execution.

| Node | Description |
|---|---|
| [Conditions](./nodes/conditions.md) | Branch execution based on one or more conditions |
| [For Loop](./nodes/for-loop.md) | Iterate over a list of items or repeat N times |
| [Wait](./nodes/wait.md) | Pause execution for a duration or until an event |
| [Human in the Loop](./nodes/human-in-the-loop.md) | Pause and require a human approval to continue |

---

### AI Nodes

AI nodes integrate language models and AI agents into your orchestration. They support multi-modal operations and can connect to other nodes as tools.

| Node | Description |
|---|---|
| [AI Agent](./nodes/ai-agent.md) | Call any LLM provider to generate text or images |
| [SubVerse Agents](./nodes/subverse-agents.md) | Execute SubVerse AI agents over voice, WhatsApp, email, or chat |

---

## Connection Types

Nodes communicate over two types of connections:

| Type | Description |
|---|---|
| **Main** | The primary data flow between nodes — carries JSON data from one node to the next |
| **AI Tool** | Connects tool nodes to an AI Agent node, making them callable by the agent during reasoning |

<Note>
  AI Tool connections are only available on the **AI Agent** node. Connect any action or logic node as a tool to give the agent the ability to call it autonomously.
</Note>

---

## Data Flow and `{{ }}` Expressions

Data moves between nodes as structured JSON. Reference any upstream node's output in a parameter field using the `{{ }}` expression syntax:

```
{{ nodeName.fieldName }}
{{ nodeName.nested.field }}
{{ forLoop.item.email }}
```

Every node parameter that accepts expressions shows a **⚡ link icon** when hovered. Click it to open the field picker, which shows all available outputs from upstream tested nodes — click any field to insert the expression automatically.

<Tip>
  See [Dynamic Inputs](./dynamic-inputs.md) for the full guide on expressions, the field picker, and common patterns.
</Tip>

---

## Node Parameters

All nodes share a common parameter structure:

| Property | Description |
|---|---|
| **Display Name** | Label shown on the canvas |
| **Node Name** | Internal identifier used in `{{ }}` expression references |
| **Credentials** | Stored authentication details for external services |
| **Parameters** | Node-specific configuration fields |

Parameters support static values, `{{ }}` expressions, and dynamic option loading from connected external services.
