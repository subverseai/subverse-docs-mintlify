# Slack Trigger

The **Slack Trigger** starts an orchestration when a Slack event occurs — such as a new message in a channel, a direct message to a bot, a reaction added, or a file shared.

![Slack Trigger Node](/images/agentverse/slack-tigger-node.png)

---

## Use Cases

- Respond to bot commands or mentions in Slack channels
- Trigger AI processing when a user sends a message to a channel
- Automate workflows based on Slack reactions or file uploads
- Build Slack bots powered by AgentVerse orchestrations

---

## Credentials

This node requires a **Slack OAuth2** credential.

To create a credential:
1. Go to **Settings → Credentials → New Credential**
2. Select **Slack OAuth2**
3. Authenticate with your Slack workspace

---

## Node Reference

### Parameters

| Parameter | Type | Description |
|---|---|---|
| **Credential** | Credential | Select or create a Slack OAuth2 credential |
| **Trigger On** | Multi-select | The Slack event types to listen for (default: `Any Event`) |

### Trigger On Options

| Option | Description |
|---|---|
| `Any Event` | Fires on all Slack events delivered to the webhook |
| `Message` | A message is posted in a channel or DM |
| `Bot Mention` | The bot is @mentioned in a channel |
| `Reaction Added` | A user adds a reaction emoji to a message |
| `File Shared` | A file is uploaded and shared in a channel |
| `Channel Created` | A new channel is created in the workspace |
| `Member Joined Channel` | A user joins a channel |

### Options

| Option | Description |
|---|---|
| **Resolve IDs** | When enabled, resolves Slack user/channel IDs to their human-readable names and returns them alongside the IDs |
| **Usernames or IDs to Ignore** | Events from these users will not trigger the orchestration |

### Webhook URL

The Slack Trigger displays a unique **Webhook URL** in the node panel. Configure this URL in your Slack app's **Event Subscriptions** settings to route Slack events to AgentVerse.

---

## Output Data

The trigger outputs the full Slack event payload:

```json
{
  "type": "message",
  "text": "Hey @bot, summarize this document",
  "user": "U012AB3CD",
  "channel": "C012AB3CD",
  "ts": "1678901234.000100",
  "team": "T012AB3CD"
}
```

Reference fields in downstream nodes:

```
{{ slackTrigger.text }}
{{ slackTrigger.user }}
{{ slackTrigger.channel }}
```

---

## Related Nodes

- [Slack](./slack.md) — Send messages and interact with Slack within an orchestration
- [AI Agent](./ai-agent.md) — Process the Slack message with an LLM
