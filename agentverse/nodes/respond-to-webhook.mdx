# Respond to Webhook

The **Respond to Webhook** node sends a custom HTTP response back to the caller of a [Webhook Trigger](./webhook.md). It is used when you need full control over the HTTP response — custom status codes, headers, or body content.

![Respond to Webhook Node](/images/agentverse/action-respond-to-webhook.png)

---

## Use Cases

- Return a custom JSON response to an API caller after processing
- Respond with a specific HTTP status code (e.g. `201 Created`, `400 Bad Request`)
- Set custom response headers (e.g. `Content-Type`, `X-Request-ID`)
- Build synchronous webhook endpoints that return processed data

---

## Prerequisites

The orchestration's Webhook Trigger must have **Response Mode** set to `Using Respond to Webhook Node`. If the response mode is set to `Immediately` or `When Last Node Finishes`, this node has no effect.

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Respond With** | Select | Yes | The format of the response body (see below) |
| **Response Body** | String / JSON | Conditional | The body to return (required for `JSON`, `Text`, `Binary`) |
| **Response Code** | Number | No | HTTP status code (default: `200`) |
| **Response Headers** | Key-Value | No | Additional headers to include in the response |

### Respond With Options

| Option | Description |
|---|---|
| `All Incoming Items` | Return the full output of all upstream nodes as JSON |
| `First Incoming Item` | Return only the first item from the upstream output |
| `JSON` | Return a custom JSON body |
| `Text` | Return a plain text body |
| `Binary` | Return a binary file (e.g. an image or PDF) |
| `No Data` | Return an empty response with just a status code |

---

## Example: Return a Custom JSON Response

Configuration:

| Field | Value |
|---|---|
| **Respond With** | `JSON` |
| **Response Code** | `200` |
| **Response Body** | `{ "status": "success", "orderId": "{{ airtable.id }}" }` |

Resulting HTTP response:

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "status": "success",
  "orderId": "recXXXXXXXXXXXXXX"
}
```

---

## Example: Return a 400 Error

| Field | Value |
|---|---|
| **Respond With** | `JSON` |
| **Response Code** | `400` |
| **Response Body** | `{ "error": "Invalid request", "message": "{{ conditions.reason }}" }` |

---

## Related Nodes

- [Webhook Trigger](./webhook.md) — The trigger node this node responds to
- [Conditions](./conditions.md) — Branch before responding based on orchestration logic
