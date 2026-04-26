# Lab 1: Trimodal Inference Engine

This lab establishes the foundational "Inference Brain" for the AI Home Lab using **Ollama** containerized with NVIDIA GPU acceleration.

## Model Choice: Gemma 4 (E2B)
- **Architecture:** Trimodal (Text, Image, Audio) reasoning engine released April 2026.
- **Size:** 5.1B parameters (Q4_K_M Quantization).
- **Key Feature:** **Reasoning/Thinking Mode** - The model generates a `<thought>` block to decompose complex logic before providing a final response.
- **Hardware Performance:** 100% VRAM offloading on NVIDIA GPU (12GB).

## Infrastructure
- **Dockerized:** Ensures environment parity and isolation.
- **GPU Passthrough:** Utilizes `nvidia-container-runtime` for hardware-accelerated inference.
- **Persistence:** Bind-mounted `models/` directory ensures weights survive container lifecycle events.

## Setup & Usage
1. Navigate to this directory: `cd labs/lab1-inference`
2. Start the engine: `docker compose up -d`
3. Pull the model: `docker exec -it ollama ollama run gemma4:e2b`

## API Validation
The engine exposes a REST API at `http://localhost:11434/api/generate` for integration with Lab 2 (RAG) and Lab 3 (n8n).
