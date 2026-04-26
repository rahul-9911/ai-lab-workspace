# AI Home Lab Workspace

Enterprise-grade AI infrastructure built with Docker, Ollama, Qdrant, and n8n.

## Status
- [x] **Lab 1: Trimodal Inference Engine (Gemma 4:E2B)** - **COMPLETE**
- [x] **Lab 2: Advanced Hybrid Memory (Qdrant)** - **COMPLETE**
- [x] **Lab 3: Agentic Orchestration (n8n)** - **COMPLETE**
- [x] **Lab 4: Multimodal Analysis** - **COMPLETE**
- [x] **Lab 5: Parameter-Efficient Fine-Tuning (LoRA)** - **COMPLETE**


## Hardware Profile
- **GPU:** 12GB VRAM
- **RAM:** 64GB
- **Host:** Dell T5810

## Setup & Quick Start

### 1. Prerequisites
- **Docker & Docker Compose**
- **NVIDIA Container Toolkit** (for GPU acceleration)
- **Git LFS** (recommended for model files)

### 2. Infrastructure Setup
Create the shared network for all containers to communicate:
```bash
docker network create ai-network
```

### 3. Lab Execution Sequence
It is recommended to follow the labs in order:

1. **Inference:** `cd labs/lab1-inference && docker compose up -d`
2. **Memory:** `cd labs/lab2-rag && docker compose up -d`
3. **Agents:** `cd labs/lab3-agents && docker compose up -d`
4. **Finetuning:** `cd labs/lab5-finetuning && docker compose up -d`

*Note: Lab 4 uses the infrastructure from Labs 1 & 3.*

## Connectivity Map
- **Ollama:** `http://localhost:11434`
- **Qdrant:** `http://localhost:6333`
- **n8n:** `http://localhost:5678`
- **Jupyter:** `http://localhost:8888` (Token: `ai_lab_2026`)
