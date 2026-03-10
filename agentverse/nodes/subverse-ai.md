# SubVerse AI

The **SubVerse AI** node initiates and manages SubVerse AI voice calls from within an orchestration. It provides direct control over outbound voice call operations at a lower level than the [SubVerse Agents](./subverse-agents.md) node.

![SubVerse Agents Node](/images/agentverse/subverse-agent-ai-node.png)

---

## Use Cases

- Initiate outbound calls as part of a notification or follow-up workflow
- Manage and monitor SubVerse AI voice sessions programmatically
- Combine voice call operations with other orchestration steps

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Operation** | Select | Yes | The call operation to perform (see below) |
| **Agent Name** | String | Yes | The SubVerse AI agent to use for the call |
| **Customer Number** | String | Yes | The phone number to call (E.164 format) |
| **Bot Number** | String | Yes | The SubVerse AI caller ID / outbound number |
| **Customer Details** | Collection | No | Customer context to provide to the agent |
| **Wait for Completion** | Boolean | No | Pause the orchestration until the call ends |

---

## Operations

| Operation | Description |
|---|---|
| `Initiate Call` | Start an outbound voice call using a SubVerse AI agent |
| `Get Call Status` | Retrieve the current status of an ongoing call |
| `End Call` | Terminate an active call |

---

## Output Data

For `Initiate Call`:

```json
{
  "callId": "call_XXXXXXXXX",
  "status": "initiated",
  "agentName": "Sales Agent",
  "customerNumber": "+919876543210",
  "botNumber": "+911234567890",
  "initiatedAt": "2025-03-10T09:00:00.000Z"
}
```

When **Wait for Completion** is enabled, the output also includes the completed call details:

```json
{
  "callId": "call_XXXXXXXXX",
  "status": "completed",
  "outcome": "resolved",
  "duration": 145,
  "transcript": [ ... ],
  "extractedData": { ... }
}
```

---

## SubVerse AI vs SubVerse Agents

| Feature | SubVerse AI | SubVerse Agents |
|---|---|---|
| **Channels** | Voice only | Voice, WhatsApp, Email, Chat |
| **Control** | Fine-grained (initiate, get status, end) | High-level (execute and wait) |
| **Use when** | You need explicit call lifecycle control | You want a single node to run an agent conversation end-to-end |

---

## Related Nodes

- [SubVerse AI Trigger](./subverse-ai-trigger.md) — Trigger an orchestration when a call completes
- [SubVerse Agents](./subverse-agents.md) — Higher-level multi-channel agent execution
- [Conditions](./conditions.md) — Branch based on call status or outcome
