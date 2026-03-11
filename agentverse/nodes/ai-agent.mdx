# AI Agent

The **AI Agent** node calls a large language model to generate text or images. It supports any LLM provider, configurable system instructions, tool connections, and multi-modal operations.

![AI Agent Node](/images/agentverse/ai-agent-ai-node.png)

---

## Use Cases

- Generate summaries, classifications, or structured data from upstream inputs
- Answer questions based on dynamic context from other nodes
- Generate images from text prompts
- Use reasoning models for complex decision-making within an orchestration
- Build autonomous agents that use other nodes as tools

---

## Node Reference

### Parameters

| Parameter | Type | Required | Description |
|---|---|---|---|
| **Provider** | Select | Yes | The LLM provider to use: `OpenAI`, `Anthropic`, `Google`, or `Custom` |
| **Model** | String | Yes | The model ID (e.g. `gpt-4o`, `claude-3-5-sonnet-20241022`, `gemini-1.5-pro`) |
| **Operation** | Select | Yes | `Generate a text response` or `Generate an image` |
| **Credential** | Credential | Yes | API key credential for the selected provider |
| **Instructions** | String | No | System instructions that guide the AI behavior |
| **Prompt** | String | Yes | The user message or input to the model |
| **Reasoning Effort** | Select | No | `Low`, `Medium`, or `High` — applicable to GPT-5, o-series, and other reasoning models |
| **Service Tier** | Select | No | The API service tier to use for the request |
| **Max Tokens** | Number | No | Maximum tokens in the response |
| **Temperature** | Number | No | Sampling temperature (0–2). Higher = more creative. |
| **Timeout** | Number | No | Maximum time to wait for a response (in seconds) |

---

## Providers

| Provider | Credential Type | Notes |
|---|---|---|
| `OpenAI` | OpenAI API Key | Supports GPT-4, GPT-4o, o1, DALL-E image generation |
| `Anthropic` | Anthropic API Key | Supports Claude 3, Claude 4 models |
| `Google` | Google AI API Key | Supports Gemini 1.5, Gemini 2 models |
| `Custom` | Bearer Token / API Key | Use any OpenAI-compatible API endpoint |

---

## Operations

### Generate a text response

Calls the model with system instructions and a user prompt. Returns the generated text response.

| Field | Description |
|---|---|
| **Instructions** | System instructions that set the model's persona or task context |
| **Prompt** | The user message. Supports template expressions (e.g. `{{ webhook.body.message }}`). |
| **Reasoning Effort** | Controls the depth of reasoning for supported models (GPT-5, o-series). |

### Generate Image

Generates an image from a text description (requires an image-capable model, e.g. DALL-E 3).

| Field | Description |
|---|---|
| **Prompt** | Text description of the image to generate |
| **Image Size** | Output image dimensions (e.g. `1024x1024`, `1792x1024`) |
| **Quality** | `Standard` or `HD` |
| **Style** | `Vivid` or `Natural` |

---

## Tool Connections (AI Tool Edges)

Connect other nodes to the AI Agent via an **AI Tool** edge to give the agent the ability to call those nodes during reasoning. The agent autonomously decides when and how to use each tool.

![AI Agent with Tools](/images/agentverse/ai-agent-tools.png)

Example: Connect an **Airtable** node and an **HTTP Request** node as tools. The agent will query Airtable or call the API as needed to answer the user's request.

---

## Output Data

For `Generate Text`:

```json
{
  "text": "The primary benefits of AI automation include...",
  "model": "gpt-4o",
  "usage": {
    "promptTokens": 245,
    "completionTokens": 87,
    "totalTokens": 332
  },
  "finishReason": "stop"
}
```

Reference in downstream nodes:

```
{{ aiAgent.text }}
{{ aiAgent.usage.totalTokens }}
```

For `Generate Image`:

```json
{
  "imageUrl": "https://oaidalleapiprodscus.blob.core.windows.net/...",
  "revisedPrompt": "..."
}
```

---

## Related Nodes

- [SubVerse Agents](./subverse-agents.md) — Run a full multi-turn SubVerse AI agent with channel support
- [Conditions](./conditions.md) — Branch based on AI output
- [Slack](./slack.md) — Send the generated text to a Slack channel
