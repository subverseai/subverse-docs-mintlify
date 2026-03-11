# AI Nodes

AI nodes integrate large language models and autonomous AI agents into your orchestrations. They can generate text, process images, call tools, and execute multi-turn agent conversations across multiple channels.

---

## Available AI Nodes

| Node | Description |
|---|---|
| [AI Agent](./nodes/ai-agent.md) | Generate text or images using any LLM provider |
| [SubVerse Agents](./nodes/subverse-agents.md) | Execute SubVerse AI agents over voice, WhatsApp, email, or chat |
| [SubVerse AI](./nodes/subverse-ai.md) | Initiate and manage SubVerse AI voice calls within an orchestration |

---

## Connection Types

AI nodes support two types of connections:

| Type | Description |
|---|---|
| **Main** | Standard data flow — the primary input/output for data passed between nodes |
| **AI Tool** | Connects a node as a callable tool that an AI Agent can invoke during reasoning |

When you connect an action node (e.g. Airtable, HTTP Request) to an AI Agent node via an **AI Tool** connection, the agent can choose to call that node as part of its reasoning process — enabling fully autonomous, tool-using agents.

---

## LLM Providers

AgentVerse AI nodes support any LLM provider. Customers can bring their own API credentials for:

- OpenAI (GPT-4, GPT-4o, o1, etc.)
- Anthropic (Claude 3.5, Claude 4, etc.)
- Google (Gemini 1.5, Gemini 2, etc.)
- Any other provider supported via API key

Provider credentials are managed in **Settings → Credentials**.
