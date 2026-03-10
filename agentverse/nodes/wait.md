# Wait

The **Wait** node pauses an orchestration run for a specified duration or until a specific date and time.

![Wait Node](/images/agentverse/wait-logic-node.png)

---

## Use Cases

- Add a delay between consecutive API calls to avoid rate limiting
- Wait for a scheduled time before sending a reminder
- Implement time-window logic (e.g. "wait until next business day")

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Wait Mode** | Toggle | Yes | `for Duration` — pause for a fixed amount of time; `Until Time` — pause until a specific date/time |
| **Amount** | Number | Conditional | Duration to wait (required for `for Duration`) |
| **Unit** | Select | Conditional | Unit of the duration: `Seconds`, `Minutes`, `Hours`, `Days` (required for `for Duration`) |
| **Date/Time** | DateTime | Conditional | Resume at this specific timestamp (required for `Until Time`) |

---

## Wait Modes

### for Duration

Pauses for a fixed duration after the node is reached.

| Field | Example |
|---|---|
| **Amount** | `5` |
| **Unit** | `Seconds` |

The orchestration resumes automatically after the specified time.

### Until Time

Pauses until an absolute date and time is reached, regardless of when the node was entered.

| Field | Example |
|---|---|
| **Date/Time** | `2025-03-15T09:00:00Z` |

---

## Output Data

The upstream node output passes through the Wait node unchanged. No data transformation occurs.

---

## Related Nodes

- [Human in the Loop](./human-in-the-loop.md) — A higher-level wait node that includes approval channel logic
- [Schedule Trigger](./schedule-trigger.md) — Start an orchestration at a specific time instead of waiting mid-run
- [For Loop](./for-loop.md) — Use Wait inside a loop to throttle iteration rate
