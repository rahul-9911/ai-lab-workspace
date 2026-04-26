# Lab 3: Agentic Orchestration (n8n)

This lab implements the "Central Nervous System" of the lab using **n8n**. It orchestrates the communication between the Gemma 4 inference engine and the Qdrant vector memory.

## Architecture
- **Orchestrator:** n8n (Self-hosted Docker version).
- **Protocol:** REST API over internal Docker networking (`ai-network`).
- **Agent Type:** Reasoning Agent with Tool-Use capabilities.

## Key Workflows
1.  **Autonomous RAG:** The agent decides when to query Qdrant based on the user's question.
2.  **Trimodal Processing:** Utilizing Gemma 4's native ability to handle multi-modal inputs routed via n8n.
3.  **Memory Management:** Implementing "Window Buffer Memory" to maintain conversation context.

## Connection Strings
- **Ollama API:** `http://ollama:11434`
- **Qdrant API:** `http://qdrant:6333`
