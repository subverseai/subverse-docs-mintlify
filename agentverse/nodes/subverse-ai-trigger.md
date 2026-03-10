# SubVerse AI Trigger

The **SubVerse AI Trigger** starts an orchestration when a SubVerse AI voice call completes. It enables post-call workflows triggered by AI-handled inbound calls.

![SubVerse AI Trigger Node](/images/agentverse/subverse-trigger-node.png)

---

## Use Cases

- Trigger a follow-up workflow after an AI voice agent completes a customer call
- Log call outcomes to Airtable or a CRM after call completion
- Send a post-call summary or follow-up message via Slack or WhatsApp
- Escalate unresolved calls to a human agent

---

## Credentials

This node uses your SubVerse AI workspace credentials, which are configured at the workspace level. No additional credential setup is required.

---

## Node Reference

### Parameters

| Parameter | Type | Description |
|---|---|---|
| **Event** | Select | The call event that triggers the orchestration |

### Event Options

| Event | Description |
|---|---|
| `Incoming Call Completed` | Fires when a SubVerse AI agent finishes handling an inbound call |

---

## Output Data

The trigger outputs the call completion payload, including transcript, outcome, and caller details:

```json
{
  "callId": "call_XXXXXXXXX",
  "botNumber": "+19876543210",
  "callerNumber": "+11234567890",
  "status": "completed",
  "duration": 145,
  "transcript": [
    { "role": "agent", "text": "Hello, how can I help you today?" },
    { "role": "user", "text": "I'd like to check my account balance." }
  ],
  "outcome": "resolved",
  "startedAt": "2025-03-10T09:00:00.000Z",
  "endedAt": "2025-03-10T09:02:25.000Z"
}
```

Reference fields in downstream nodes:

```
{{ subverseAITrigger.callerNumber }}
{{ subverseAITrigger.outcome }}
{{ subverseAITrigger.transcript }}
{{ subverseAITrigger.duration }}
```

---

## Related Nodes

- [SubVerse Agents](./subverse-agents.md) — Execute SubVerse AI agents for outbound calls or other channels
- [SubVerse AI](./subverse-ai.md) — Manage SubVerse AI voice interactions within an orchestration
- [Slack](./slack.md) — Send post-call notifications to a Slack channel
