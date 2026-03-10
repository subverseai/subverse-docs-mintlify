# WhatsApp Business Cloud

The **WhatsApp Business Cloud** node lets you send messages, share media, and manage contacts via the WhatsApp Business API from within an orchestration.

![WhatsApp Business Cloud Node](/images/agentverse/whatsapp-action-node.png)

---

## Credentials

This node requires a **WhatsApp** credential.

To create a credential:
1. Go to **Settings → Credentials → New Credential**
2. Select **WhatsApp**
3. Enter your WhatsApp Business API access token and phone number ID

---

## Operations

### Message

| Operation | Description |
|---|---|
| `Send Text` | Send a plain text message to a phone number |
| `Send Template` | Send an approved WhatsApp message template |
| `Send Media` | Send an image, video, audio, or document |
| `Send Location` | Send a location pin |
| `Send Reaction` | React to a message with an emoji |
| `Mark as Read` | Mark an incoming message as read |

### Contact

| Operation | Description |
|---|---|
| `Get` | Retrieve contact information |

---

## Parameters: Send Text

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Credential** | Credential | Yes | Select or create a WhatsApp credential |
| **To** | String | Yes | Recipient phone number in E.164 format (e.g. `+919876543210`) |
| **Message** | String | Yes | The text message to send |
| **Preview URL** | Boolean | No | Enable URL link previews in the message |

## Parameters: Send Template

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Messaging Product** | String | Yes | Always `whatsapp` |
| **Sender Phone Number (or ID)** | Select | Yes | The WhatsApp Business account phone number or ID the message is sent from |
| **Recipient's Phone Number** | String | Yes | The recipient's phone number |
| **Template** | Select | Yes | The approved message template to send (select from list) |
| **Language Code** | String | Yes | Template language (e.g. `en_US`) |
| **Components** | Collection | No | Template variable substitutions (header, body, buttons) |

## Parameters: Send Media

| Parameter | Type | Required | Description |
|---|---|---|---|
| **To** | String | Yes | Recipient phone number |
| **Media Type** | Select | Yes | `Image`, `Video`, `Audio`, `Document`, `Sticker` |
| **Media URL** | String | Yes | Public URL of the media file |
| **Caption** | String | No | Caption text to include with the media |
| **Filename** | String | No | Display filename for documents |

---

## Output Data

A successful `Send Text` operation returns:

```json
{
  "messaging_product": "whatsapp",
  "contacts": [
    {
      "input": "+919876543210",
      "wa_id": "919876543210"
    }
  ],
  "messages": [
    {
      "id": "wamid.XXXXXXXXXXXX"
    }
  ]
}
```

Reference in downstream nodes:

```
{{ whatsapp.messages[0].id }}
{{ whatsapp.contacts[0].wa_id }}
```

---

## Related Nodes

- [WhatsApp Trigger](./whatsapp-trigger.md) — Trigger on incoming WhatsApp messages
- [SubVerse Agents](./subverse-agents.md) — Delegate WhatsApp conversations to a SubVerse AI agent
