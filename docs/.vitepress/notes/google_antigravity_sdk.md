---
name: google-antigravity-sdk
description: Design, configure, run, and debug autonomous AI agents and multi-agent systems using the Google Antigravity (AGY) SDK.
---
# Google Antigravity SDK Specialist

This skill provides comprehensive instructions for designing, implementing, and debugging autonomous AI agents and multi-agent systems using the Google Antigravity (AGY) SDK.

## Installation & Setup

Ensure the environment is ready for Google Antigravity operations:
-   **Verify Applicability**: Verify that using this Python SDK is appropriate for your project.
-   **Check Dependencies**: Add `google-antigravity` to your project dependencies (e.g., `requirements.txt`).
-   **Authentication Setup**: A valid `GEMINI_API_KEY` is required. You can obtain one from:
    -   Google AI Studio: `https://aistudio.google.com/app/api-keys`
    -   Pass keys in code: `LocalAgentConfig(api_key="...")` or set them via the environment.

## Agent Loop & Multi-Agent orchestration

Use the standard asynchronous agent context manager for single-turn or multi-turn chat loops:

```python
import asyncio
from google.antigravity import Agent, LocalAgentConfig

async def run_agent():
    config = LocalAgentConfig(model="gemini-2.5-pro")
    async with Agent(config) as agent:
        response = await agent.chat("Initialize 114-Chakra network routing state.")
        print(await response.text())

asyncio.run(run_agent())
```

### Delegation (Subagents)

Agents can spawn specialized subagents to delegate complex execution steps:

```python
async with agent.spawn_subagent(role="Database Researcher") as subagent:
    response = await subagent.chat("Scan for inactive database partitions.")
```

## Tool & MCP Integration

Extend agent capabilities with custom Python functions or Model Context Protocol (MCP) servers:
-   **Custom Tools**: Define standard Python functions and attach them to the agent config.
-   **MCP Integration**: Configure stdio or SSE servers inside the agent’s config to expose remote databases and APIs dynamically.
