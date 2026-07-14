# Action Nodes

Action nodes perform operations on external services — sending messages, reading or writing data, making API calls, and uploading files.

Action nodes receive data from upstream nodes, perform their operation, and pass the result to downstream nodes.

---

## Available Action Nodes

| Node | Service | Description |
|---|---|---|
| [Slack](../nodes/slack.mdx) | Slack | Send messages, manage channels, users, and files |
| [Airtable](../nodes/airtable.mdx) | Airtable | Read, create, update, and delete records |
| [Shopify](../nodes/shopify.mdx) | Shopify | Manage orders, products, customers, and inventory |
| [WhatsApp](../nodes/whatsapp.mdx) | WhatsApp | Send messages and manage contacts |
| [Freshdesk](../nodes/freshdesk.mdx) | Freshdesk | Manage support tickets, notes, and replies |
| [HTTP Request](../nodes/http-request.mdx) | Any API | Make HTTP requests to any external endpoint |
| [Send Email](../nodes/email.mdx) | SMTP | Send emails through any SMTP server |
| [File Upload](../nodes/file-upload.mdx) | Cloud Storage | Upload files to S3 cloud storage |
| [Respond to Webhook](../nodes/respond-to-webhook.mdx) | AgentVerse | Send a custom HTTP response back to a webhook caller |

---

## Credentials

Most action nodes require credentials to authenticate with the external service. Credentials are managed in **Settings → Credentials** and referenced by nodes in an orchestration.

Each node page lists the credential type(s) it supports.
