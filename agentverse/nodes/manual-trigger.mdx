# Manual Trigger (Starter)

The **Starter** node is AgentVerse's combined manual and scheduled trigger. In **Manual Trigger** mode it starts an orchestration immediately when you click **Trigger Now** from the canvas — used for testing, on-demand tasks, and orchestrations that do not need to respond to an event.

> The same Starter node also supports **Schedule At** mode. See [Schedule Trigger](./schedule-trigger.md).

![Starter Node — Manual Trigger mode](/images/agentverse/starter-node.png)

---

## Use Cases

- Test an orchestration during development
- Run one-off data processing tasks on demand
- Trigger workflows that take user-uploaded files as input

---

## Node Reference

### Parameters

| Parameter | Type | Description |
|---|---|---|
| **Trigger Mode** | Select | Set to `Manual Trigger` to enable on-demand execution |
| **Upload Data Files** | Files | Optional XLSX, CSV, or JSON files to inject as input data |

There are no required parameters. Click **Trigger Now** on the node canvas to execute immediately, or use **Test (N Records)** to run with a preview of your uploaded data.

---

## How It Works

When you click **Trigger Now** on the Starter node:

1. AgentVerse creates a new Orchestration Run immediately.
2. Any uploaded files (XLSX, CSV, JSON) are parsed and injected as the trigger output.
3. Execution proceeds through all downstream nodes.
4. The run result appears in the **Orchestration Runs** panel in real time.

---

## Output Data

When no files are uploaded, the output is a minimal execution context:

```json
{
  "executionMode": "manual",
  "triggeredAt": "2025-03-10T09:00:00.000Z"
}
```

When files are uploaded, each file is available as a binary item:

```json
{
  "binary": {
    "file": {
      "data": "<base64>",
      "mimeType": "application/pdf",
      "fileName": "report.pdf"
    }
  }
}
```

---

## Testing vs. Production

| Mode | Description |
|---|---|
| **Test Mode** | Run the orchestration from the canvas editor. Uses test data and does not count toward production run limits. |
| **Production Run** | Triggered by activating the orchestration and clicking Run from the runs list. Uses live credentials and counts as a production execution. |

---

## Related Nodes

- [Schedule Trigger](./schedule-trigger.md) — Run automatically on a time-based schedule
- [Webhook Trigger](./webhook.md) — Trigger from an external HTTP event
