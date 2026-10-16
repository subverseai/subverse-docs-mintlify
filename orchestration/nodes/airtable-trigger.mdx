# Airtable Trigger

The **Airtable Trigger** starts an orchestration when a record is created, updated, or deleted in an Airtable base.

![Airtable Trigger Node](/images/agentverse/airtable-trigger-node.png)

---

## Use Cases

- Sync Airtable records to another service when new rows are added
- Notify a Slack channel when a CRM record is updated
- Trigger an AI agent when new data arrives in Airtable

---

## Credentials

This node requires an **Airtable** credential. Two credential types are supported:

| Type | Description |
|---|---|
| **Airtable Personal Access Token** | Token-based authentication using an Airtable API token |
| **Airtable OAuth2** | Platform-managed OAuth2 — sign in with your Airtable account |

To create a credential, go to **Settings → Credentials → New Credential** and select the Airtable credential type.

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Credential** | Credential | Yes | Select or create an Airtable credential |
| **Base** | Resource Locator | Yes | The Airtable base to monitor — select from list, by URL, or by ID |
| **Table** | Resource Locator | Yes | The table within the base to monitor — select from list, by URL, or by ID |
| **Trigger Field** | String | Yes | A **Created Time** or **Last Modified Time** field used to detect new/updated records. Your table schema must include one of these field types for the trigger to work correctly. |
| **Download Attachments** | Boolean | No | When enabled, downloads any attachment fields defined in **Additional Fields** |
| **Additional Fields — Fields** | String | No | Comma-separated list of field names to return in the output (returns all fields by default) |

---

## Output Data

The trigger outputs the full record that triggered the event:

```json
{
  "id": "recXXXXXXXXXXXXXX",
  "createdTime": "2025-03-10T09:00:00.000Z",
  "fields": {
    "Name": "Acme Corp",
    "Status": "Active",
    "Revenue": 150000
  }
}
```

Reference fields in downstream nodes:

```
{{ airtableTrigger.fields.Name }}
{{ airtableTrigger.fields.Status }}
{{ airtableTrigger.id }}
```

---

## Related Nodes

- [Airtable](./airtable.md) — Read and write Airtable records within an orchestration
- [Conditions](./conditions.md) — Branch based on record field values
