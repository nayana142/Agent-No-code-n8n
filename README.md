# Agent-No-code-n8n

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/139669d4-c933-444c-8e18-a25905acff63" />

In n8n, an AI agent is a dynamic, decision-making entity within a workflow that uses a large language model (LLM) to intelligently interpret requests and decide what actions to take. 
Unlike traditional automation that follows predefined steps, n8n agents can reason, adapt, and autonomously use other tools and integrations to achieve a goal.


## Core capabilities
* Built on LangChain: N8n integrates with LangChain, a popular framework for building with LLMs, making it easier to create complex agents without writing extensive code.
* Decision-making: Agents can decide which tools to use to fulfill a request. For example, a customer service agent can analyze a query and autonomously decide whether to use a tool to look up a customer's order or to create a support ticket.
* Multi-agent systems: You can build sophisticated systems where different AI agents specialize in specific tasks. A "gatekeeper" agent can receive a request, then delegate parts of it to other, more specialized agents, such as a research agent or a summarizing agent.
* Memory: N8n agents can be configured with memory nodes to remember context throughout a conversation, enabling more natural and coherent interactions with users.
* Custom tools: To perform actions beyond the built-in integrations, you can create custom tools using the HTTP Request node or turn other n8n workflows into tools that an agent can call.
  
## How n8n agents work in a workflow
1. Start with a trigger: A workflow is initiated by a trigger node, such as a new chat message, a webhook, or a scheduled time.
2. Add the AI Agent node: The core of the agentic workflow is the AI Agent node, which receives the input from the trigger.
3. Define behavior: Inside the AI Agent node, you configure its behavior using system prompts and connect it to your chosen large language model (e.g., GPT-4).
4. Provide tools: You add other n8n nodes as "tools" for the agent to use. These can include integrations with apps like Slack, Google Sheets, or a custom HTTP Request node for external APIs.
5. Agent takes action: Based on the user's input and the tools available, the agent uses the LLM to decide on the best course of action. It can run multiple times in a single workflow execution to set up, call a tool, and process the response. 
