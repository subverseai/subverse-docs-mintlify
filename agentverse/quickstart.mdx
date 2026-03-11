---
title: 'Quickstart'
description: 'Build your first AgentVerse orchestration in 10 minutes — webhook trigger, AI processing, Slack notification'
---

# Quickstart

Build your first orchestration: receive a webhook, process the payload with an AI Agent, and send the result to Slack.

**Time to complete:** ~10 minutes

---

## Prerequisites

- Access to an AgentVerse workspace
- A Slack workspace with a connected credential (you'll create it in Step 4)
- An LLM provider API key (OpenAI, Anthropic, Google, or any supported provider)

---

## What You'll Build

```
[Webhook Trigger] → [AI Agent] → [Slack]
```

1. A webhook receives an incoming HTTP POST with a user message
2. An AI Agent processes the message and generates a response
3. The response is sent to a Slack channel

---

## Steps

<Steps>
  <Step title="Create a New Orchestration">
    1. Open **AgentVerse** from the SubVerse AI dashboard.
    2. Click **New Orchestration**.
    3. Give it a name, e.g. `Webhook AI Slack Notification`.
    4. Click **Create**.

    The canvas opens with an empty orchestration ready to build.
  </Step>

  <Step title="Add a Webhook Trigger">
    1. On the canvas, click **+** to open the node picker.
    2. Under **Trigger**, select **Webhook**.
    3. Set **HTTP Method** to `POST`.
    4. Set **Response Mode** to `When Last Node Finishes`.
    5. Copy the **Webhook URL** shown in the node — you will need this to test.

    <Note>
      The webhook URL is unique per orchestration. It only becomes active after you activate the orchestration in Step 5.
    </Note>
  </Step>

  <Step title="Add an AI Agent Node">
    1. Click **+** on the right edge of the Webhook node.
    2. Under **AI**, select **AI Agent**.
    3. Configure the node:

    | Field | Value |
    |---|---|
    | **Provider** | Your preferred LLM provider (e.g. OpenAI) |
    | **Model** | Your preferred model (e.g. `gpt-4o`) |
    | **Operation** | `Generate Text` |
    | **Instructions** | `You are a helpful assistant. Respond concisely to the user message.` |

    4. In the **Prompt** field, reference the incoming message from the webhook using the `{{ }}` expression syntax:

    ```
    {{ webhook.body.message }}
    ```

    <Tip>
      Test the Webhook node first by clicking **Test**, then use the ⚡ link icon next to the Prompt field to visually browse and insert available fields. See [Dynamic Inputs](./dynamic-inputs.md) for details.
    </Tip>
  </Step>

  <Step title="Configure the Slack Node">
    1. Click **+** on the right edge of the AI Agent node.
    2. Under **Action**, select **Slack**.
    3. Select operation **Send a Message**.
    4. Connect or create a **Slack credential**:
       - Click **Create New Credential**
       - Authenticate with your Slack workspace via OAuth
    5. Configure the message:

    | Field | Value |
    |---|---|
    | **Channel** | `#general` (or your target channel) |
    | **Message Text** | `{{ aiAgent.text }}` |
  </Step>

  <Step title="Activate and Test">
    1. Click **Activate** in the top toolbar to enable the webhook listener.
    2. Send a test request:

    ```bash
    curl -X POST https://<your-webhook-url> \
      -H "Content-Type: application/json" \
      -d '{"message": "Summarise the benefits of AI automation in one sentence."}'
    ```

    3. Open the **Runs** tab to see the live execution trace.
    4. Verify the Slack channel received the AI-generated message.

    <img
      style={{ borderRadius: '0.5rem' }}
      src="/images/agentverse/orchestration-run.png"
    />
  </Step>
</Steps>

---

## What Happened

| Step | Node | Action |
|---|---|---|
| 1 | Webhook | Received POST, extracted `body.message` |
| 2 | AI Agent | Sent prompt to LLM, received text response |
| 3 | Slack | Posted the AI response to the Slack channel |

---

## Next Steps

<CardGroup cols={2}>
  <Card title="Dynamic Inputs" icon="link" href="./dynamic-inputs">
    Learn how to link node outputs to parameters using `{{ }}` expressions
  </Card>
  <Card title="Conditions Node" icon="code-branch" href="./nodes/conditions">
    Branch your orchestration based on AI output or data values
  </Card>
  <Card title="SubVerse Agents" icon="robot" href="./nodes/subverse-agents">
    Replace the AI Agent with a full multi-channel SubVerse AI agent
  </Card>
  <Card title="Monitoring" icon="chart-line" href="./monitoring">
    Track runs, inspect traces, and set up failure alerts
  </Card>
</CardGroup>
