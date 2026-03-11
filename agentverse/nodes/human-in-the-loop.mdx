# Human in the Loop

The **Human in the Loop** node pauses an orchestration run and sends an approval request to a human via Slack or email. Execution resumes only after the reviewer approves or rejects the request — or after a configured timeout.

![Human In The Loop Node](/images/agentverse/human-in-the-loop-logic-node.png)

---

## Use Cases

- Require manager approval before processing a large transaction
- Route AI-generated content for human review before publishing
- Create an approval step in a multi-stage data pipeline
- Escalate flagged support tickets to a human agent

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Approval Channel** | Select | Yes | How to send the approval request: `Slack` or `Email` |

### Email Channel Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Email Addresses** | String | Yes | One or more approver email addresses, separated by commas |
| **Subject** | String | No | Email subject line (default: `Workflow Approval Required`) |
| **Message** | String | No | Body message for the approval email (default: `Please review and approve this workflow action.`) |

### Slack Channel Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Slack Credential** | Credential | Yes | Select or create a Slack OAuth2 credential |
| **Send To** | Select | Yes | `Channel` or `User` |
| **Slack Channel** | String | Conditional | Channel name or ID (required when `Send To` is `Channel`) |
| **Slack User** | String | Conditional | User ID or email (required when `Send To` is `User`) |
| **Message** | String | No | Custom message to include in the approval request |

### Timeout Settings

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Value** | Number | Yes | How long to wait for a response before timing out (default: `24`) |
| **Unit** | Select | Yes | Unit for the timeout: `Minutes`, `Hours`, `Days` (default: `Hours`) |
| **On Timeout** | Select | Yes | What to do if no response is received: `Approve` or `Reject` |

---

## How It Works

1. The node sends an approval request to the configured channel (Slack or email).
2. The request includes **Approve** and **Reject** action buttons.
3. The orchestration run is paused and waits for a response.
4. When the approver clicks **Approve** or **Reject**, execution resumes on the corresponding branch.
5. If no response arrives within the timeout window, the **Default Action** is applied.

---

## Output Branches

The node has two output branches:

| Branch | Condition |
|---|---|
| **Approved** | The approver clicked Approve, or timed out with Default Action = Approve |
| **Rejected** | The approver clicked Reject, or timed out with Default Action = Reject |

Connect different downstream nodes to each branch to handle both outcomes.

---

## Output Data

The output includes the original upstream data plus the reviewer's decision:

```json
{
  "decision": "approved",
  "reviewer": "alice@example.com",
  "reviewedAt": "2025-03-10T09:15:00.000Z",
  "comment": "Looks good, proceed."
}
```

Reference in downstream nodes:

```
{{ humanInTheLoop.decision }}
{{ humanInTheLoop.reviewer }}
{{ humanInTheLoop.comment }}
```

---

## Related Nodes

- [Wait](./wait.md) — A lower-level pause node for custom webhook-based resume flows
- [Conditions](./conditions.md) — Branch based on the approval outcome
- [Slack](./slack.md) — Send a follow-up Slack message after the decision
