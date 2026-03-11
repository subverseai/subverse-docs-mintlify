# Logic Nodes

Logic nodes control the flow of execution within an orchestration. They route data through branches, iterate over collections, pause execution, and coordinate human decisions.

---

## Available Logic Nodes

| Node | Description |
|---|---|
| [Conditions](./nodes/conditions.md) | Branch execution based on one or more rule-based or AI-evaluated conditions |
| [For Loop](./nodes/for-loop.md) | Iterate over an array of items or repeat N times |
| [Wait](./nodes/wait.md) | Pause execution for a duration, until a time, or until a webhook is received |
| [Human in the Loop](./nodes/human-in-the-loop.md) | Pause and require a human to approve before execution continues |

---

## How Logic Nodes Affect Data Flow

Logic nodes can split and rejoin data streams. When an orchestration branches (e.g. via Conditions), each branch executes independently. If branches need to be merged, use a downstream node that processes all available inputs.

Loop nodes wrap a sub-graph and re-execute it for each item in a collection. The loop's output is an array of results — one per iteration.
