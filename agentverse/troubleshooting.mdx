# Troubleshooting

This page covers common issues encountered when building and running AgentVerse orchestrations, along with steps to diagnose and resolve them.

---

## General Debugging Workflow

1. Open the **Orchestration Runs** panel and find the failed run.
2. Click the run to open the **Run Detail** view.
3. Inspect the **Node Execution Trace** — identify the first node with an `Error` status.
4. Expand the node row to view the full error message and the input data it received.
5. Use the information below to resolve the specific error type.

---

## Common Errors

### Orchestration Does Not Trigger

**Symptom:** No runs appear in the Orchestration Runs panel when the expected event occurs.

| Cause | Resolution |
|---|---|
| Orchestration is not activated | Click **Activate** in the top toolbar. A deactivated orchestration will not listen for trigger events. |
| Webhook URL is incorrect | Copy the exact webhook URL from the Webhook Trigger node — use the production URL, not the test URL. |
| Cron schedule is in the wrong timezone | Check the timezone setting on the Schedule Trigger node. Verify that the configured time is correct for your target timezone. |
| Slack / WhatsApp trigger app is not installed | Ensure the bot has been added to the target channel or workspace. Re-authenticate the credential if needed. |

---

### Node Failed: Credential Error

**Symptom:** A node fails with `401 Unauthorized`, `403 Forbidden`, or `Invalid API key`.

| Cause | Resolution |
|---|---|
| Credential has expired | Go to **Settings → Credentials**, find the credential, and re-authenticate or update the token. |
| Credential lacks required permissions/scopes | Check the node's documentation for required scopes and update your OAuth app or API key. |
| Wrong credential selected | Open the node configuration and confirm the correct credential is selected. |

---

### Node Failed: Template Resolution Error

**Symptom:** A node fails with `Cannot read property of undefined` or produces empty/unexpected values.

**Cause:** A `{{ }}` expression references a field that does not exist in the upstream node's output.

**Resolution:**

1. Open the failed run and expand the upstream node to view its actual output.
2. Verify the field names match exactly (case-sensitive).
3. Use dot notation for nested fields: `{{ webhook.body.data.userId }}`
4. Use a fallback value for optional fields: `{{ webhook.body.userId || 'unknown' }}`

---

### Node Failed: HTTP Request Error

**Symptom:** HTTP Request node fails with a 4xx or 5xx status code.

| Status Code | Likely Cause | Resolution |
|---|---|---|
| `400 Bad Request` | Malformed request body or missing required fields | Check the API documentation and verify your request body format |
| `401 Unauthorized` | Missing or invalid authentication | Verify the credential and authentication method configured on the node |
| `403 Forbidden` | Insufficient API permissions | Check API key scopes or account permissions |
| `404 Not Found` | Incorrect endpoint URL | Verify the URL — check for trailing slashes, typos, or incorrect path parameters |
| `429 Too Many Requests` | Rate limit exceeded | Add a [Wait](./nodes/wait.md) node to throttle request rate |
| `5xx Server Error` | External service is unavailable | Check the service's status page; implement retry logic using a For Loop |

---

### Orchestration Run Times Out

**Symptom:** A run stays in `Running` state for a long time and then fails with a timeout error.

| Cause | Resolution |
|---|---|
| An AI Agent node takes too long | Increase the **Timeout** setting on the AI Agent node, or switch to a faster model |
| Wait node with webhook resume never received a callback | Check that the external system is posting to the correct resume URL |
| Human in the Loop awaiting approval | Check that the approval request was delivered to the correct Slack channel or email address |
| External API is slow to respond | Increase the timeout on the HTTP Request node; add retry logic |

---

### Infinite Loop

**Symptom:** A For Loop runs indefinitely and the run never completes.

| Cause | Resolution |
|---|---|
| Array input is empty (causes unexpected behavior) | Add a [Conditions](./nodes/conditions.md) node before the For Loop to check that the array is non-empty |
| Loop has no termination condition | Verify that `Iteration Count` or the `Input Array` reference is correctly set |

---

### Human in the Loop — Approval Message Not Received

**Symptom:** The Slack or email approval message is never delivered.

| Cause | Resolution |
|---|---|
| Bot is not a member of the target channel | Invite the Slack bot to the channel |
| Email is in spam | Ask the approver to check their spam folder; whitelist the sending domain |
| Incorrect channel or email configured | Open the Human in the Loop node and verify the **Slack Channel** or **To Email** field |
| Credential has expired | Re-authenticate the Slack credential in **Settings → Credentials** |

---

### SubVerse Agent Call Did Not Start

**Symptom:** A SubVerse Agents or SubVerse AI node reports a failure to initiate a call.

| Cause | Resolution |
|---|---|
| Invalid phone number format | Ensure the number is in E.164 format: `+<country-code><number>` (e.g. `+919876543210`) |
| Bot number is not configured | Verify the bot number in the SubVerse AI dashboard and ensure it is active |
| Insufficient call credits | Check your SubVerse AI account balance |

---

## Getting Help

If you cannot resolve an issue using this guide:

1. Collect the **Run ID** and **error message** from the Run Detail view.
2. Check the **Node Execution Trace** and note which node failed and what input it received.
3. Contact SubVerse AI support with this information.

---

## Related Pages

- [Monitoring](./monitoring.md) — View run history, metrics, and alerts
- [Node Types](./node-types.md) — Reference for all node parameters and behavior
