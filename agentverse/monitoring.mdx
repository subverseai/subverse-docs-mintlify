---
title: 'Monitoring'
description: 'Track orchestration runs, inspect node-level execution traces, and set up failure alerts'
---

# Monitoring

AgentVerse logs every orchestration execution in full detail — inputs, outputs, errors, and timing at both the run level and the individual node level. Use the monitoring panel to debug issues, verify behaviour, and track performance over time.

---

## Orchestration Runs

Open any orchestration and click the **Runs** tab to see all past and in-progress executions.

<img
  style={{ borderRadius: '0.5rem' }}
  src="/images/agentverse/orchestration-run.png"
/>

### Run Statuses

| Status | Description |
|---|---|
| `Running` | The orchestration is currently executing |
| `Success` | All nodes completed without errors |
| `Failed` | One or more nodes encountered an error |
| `Waiting` | The run is paused (Wait node or Human in the Loop) |
| `Cancelled` | The run was manually stopped |

### Filtering Runs

Narrow the list using:

| Filter | Description |
|---|---|
| **Status** | Show only `Success`, `Failed`, `Running`, or `Waiting` runs |
| **Date Range** | Filter by start time window |
| **Trigger Type** | Filter by how the run was initiated |
| **Run ID** | Search for a specific run by its unique ID |

---

## Run Detail View

Click any run row to open the **Run Detail** panel. This shows everything that happened during that execution.

### Run Summary

| Field | Description |
|---|---|
| **Run ID** | Unique identifier for this execution — use this when contacting support |
| **Trigger** | Which trigger started the run: `webhook`, `schedule`, or `manual` |
| **Started At / Ended At** | Timestamps for run start and completion |
| **Duration** | Total wall-clock execution time |
| **Status** | Final run outcome |

### Node Execution Trace

The trace shows every node that ran, in order:

| Column | Description |
|---|---|
| **Node** | Node name and type |
| **Status** | `Success`, `Error`, or `Skipped` |
| **Started At** | When the node began executing |
| **Duration** | How long the node took |
| **Input** | The data received by the node |
| **Output** | The data produced by the node |
| **Error** | Error message and stack trace if the node failed |

Click any node row to expand and inspect its **full input and output payloads as JSON**. This is the primary tool for debugging unexpected node behaviour.

<Tip>
  When debugging, expand both the input and output of the failing node side by side. The input tells you what data the node received; the output (or error) tells you what went wrong.
</Tip>

---

## Re-running Failed Runs

To retry a failed orchestration:

1. Find the failed run in the **Runs** panel.
2. Click the **Re-run** button (replay icon) on the right.
3. The orchestration restarts from the beginning using the same original trigger data.

<Note>
  Re-runs create a new Run ID and are logged as a separate entry — the original failed run is preserved. This means you can compare the re-run trace against the original to confirm the fix.
</Note>

---

## Alerts and Notifications

Configure alerts to be notified automatically when an orchestration fails or exceeds a duration threshold.

### Setting Up Alerts

1. Open the orchestration and navigate to **Settings → Alerts**.
2. Click **Add Alert**.
3. Configure the alert rule:

| Field | Options |
|---|---|
| **Trigger On** | `Orchestration Failed`, `Orchestration Timed Out`, `Node Error` |
| **Notify Via** | `Slack`, `Email` |
| **Destination** | Slack channel name or email address |
| **Cooldown** | Minimum time between repeated alerts for the same orchestration (prevents alert spam) |

### Alert Payload

Every alert includes:

- Orchestration name and ID
- Run ID
- Failed node name and error message
- Direct link to the run detail page

<Warning>
  Set a cooldown period for high-frequency orchestrations to avoid alert fatigue. A cooldown of 5–15 minutes is typical for production orchestrations.
</Warning>

---

## Related Pages

- [Troubleshooting](./troubleshooting.md) — Diagnose and resolve common issues
- [Quickstart](./quickstart.md) — Build and test your first orchestration
