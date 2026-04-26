# AI Home Lab Workspace

Enterprise-grade AI infrastructure built with Docker, Ollama, Qdrant, and n8n.

## Architecture
- **Lab 1:** Local Inference Engine (Ollama)
- **Lab 2:** RAG Pipeline (Qdrant)
- **Lab 3:** Agentic Workflows (n8n)
- **Lab 4:** Multimodal Analysis
- **Lab 5:** Parameter-Efficient Fine-Tuning (LoRA)

## Hardware Profile
- **GPU:** 12GB VRAM
- **RAM:** 64GB
- **Host:** Dell T5810

## Setup
1. Clone the repo.
2. Ensure NVIDIA Container Toolkit is installed.
3. `cd labs/lab1-inference && docker compose up -d`
