# File Upload

The **File Upload** node uploads files to cloud storage (S3) from within an orchestration. It supports multiple input methods — direct file, base64 string, public URL, or WhatsApp media — and returns a public download URL.

![File Upload Node](/images/agentverse/file-upload-action-node.png)

---

## Use Cases

- Store files received from a webhook or WhatsApp message in S3
- Convert base64-encoded file data to a publicly accessible URL
- Mirror files from an external URL into your own storage
- Attach uploaded file URLs to records in Airtable or Slack

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Operation** | Select | Yes | The upload operation to perform (see below) |
| **Media ID** | String | Conditional | WhatsApp media ID from the incoming message (required for `Upload WhatsApp Media`) |
| **Custom File Name** | String | No | Name for the uploaded file (auto-generated if not provided) |
| **Content Type** | String | No | MIME type of the file (auto-detected if not provided, e.g. `application/pdf`) |
| **URL Expiry (TTL)** | Number | No | How long the presigned download URL remains valid, in minutes (default: `10`) |
| **Bucket Path** | String | No | Sub-folder path within the storage bucket (default: `uploads/workflow/`) |

### Operations

| Operation | Description |
|---|---|
| `Upload WhatsApp Media` | Download a media item from WhatsApp using its media ID and upload it to storage |
| `Upload from URL` | Download a file from a public URL and upload it to storage |
| `Upload Binary` | Upload a binary file received from an upstream node |

---

## Output Data

A successful upload returns the storage URL:

```json
{
  "url": "https://subverse-storage.s3.ap-south-1.amazonaws.com/uploads/report-2025.pdf",
  "fileName": "report-2025.pdf",
  "mimeType": "application/pdf",
  "size": 204800,
  "uploadedAt": "2025-03-10T09:00:00.000Z"
}
```

Reference in downstream nodes:

```
{{ fileUpload.url }}
{{ fileUpload.fileName }}
```

---

## Related Nodes

- [WhatsApp Trigger](./whatsapp-trigger.md) — Receive a WhatsApp media message and upload the file
- [Airtable](./airtable.md) — Attach the uploaded URL to an Airtable record
- [Slack](./slack.md) — Share the file URL in a Slack message
