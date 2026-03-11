# For Loop

The **For Loop** node iterates over a collection of items or repeats a sub-graph N times. Nodes placed inside the loop body execute once per item or iteration.

![For Loop Node](/images/agentverse/for-loop-logic-node.png)

---

## Use Cases

- Process each record from an Airtable query individually
- Send a personalized Slack message to each user in a list
- Call an AI Agent once for each item in an array
- Retry an operation a fixed number of times

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Loop Mode** | Select | Yes | How to iterate: `Count` or `Array` (see below) |
| **Iteration Count** | Number | Conditional | Number of iterations (required when Mode is `Count`) |
| **Input Array** | Expression | Conditional | The array to iterate over (required when Mode is `Array`) |
| **Execution Mode** | Select | No | `Sequential` or `Parallel` — how iterations are executed |
| **Max Concurrency** | Number | No | Max parallel iterations when using `Parallel` mode (max: 10) |
| **Error Handling** | Toggle | No | `Fail Fast` — stop on first error; `Continue on Error` — log and continue |

### Loop Modes

| Mode | Description |
|---|---|
| `Count` | Run the loop body a fixed number of times. Current iteration index (`{{ $index }}`) is available. |
| `Array` | Run the loop body once for each element in an array. Current item (`{{ $item }}`) is available. |

### Execution Modes

| Mode | Description |
|---|---|
| `Sequential` | Iterations execute one at a time, in order. Each iteration waits for the previous to complete. |
| `Parallel` | Iterations execute concurrently up to `Max Concurrency`. Faster, but order of completion is not guaranteed. |

### Error Handling

| Option | Description |
|---|---|
| `Fail Fast` | Halt the loop immediately on the first error and fail the orchestration run |
| `Continue on Error` | Log the error and continue processing remaining iterations |

---

## Loop Variables

Within the loop body, use these built-in expressions:

| Variable | Description |
|---|---|
| `{{ $index }}` | Current iteration index (0-based) |
| `{{ $item }}` | Current item value (in Array mode) |
| `{{ $iteration }}` | Current iteration number (1-based) |
| `{{ $total }}` | Total number of iterations |

---

## Example: Process an Array of Records

Configuration:

```
Loop Mode: Array
Input Array: {{ airtable.records }}
Execution Mode: Sequential
```

Inside the loop body, `{{ $item.fields.Name }}` refers to the current record's `Name` field.

---

## Output Data

After the loop completes, the node outputs an array containing the results from each iteration:

```json
[
  { "result": "Processed record recAAA" },
  { "result": "Processed record recBBB" },
  { "result": "Processed record recCCC" }
]
```

---

## Related Nodes

- [Airtable](./airtable.md) — Retrieve a list of records to iterate over
- [Conditions](./conditions.md) — Branch within a loop based on per-item values
- [Wait](./wait.md) — Add a delay between iterations
