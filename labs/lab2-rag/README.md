# Lab 2: Advanced Hybrid Memory (Qdrant)

This lab deploys a high-performance **Vector Database** that serves as the "Long-Term Memory" for the AI Home Lab.

## Why Qdrant?
Qdrant was selected for its native support of **Hybrid Search**, which is the 2026 industry standard for production RAG (Retrieval-Augmented Generation).

## Key Features
- **Hybrid Search Ready:** Configured with both Dense (768-dim) and Sparse vector support to combine semantic meaning with exact keyword matching.
- **Persistence:** Data is stored in a bind-mounted `storage/` directory, ensuring index persistence across container restarts.
- **Container Networking:** Connected to `ai-network` for low-latency communication with Lab 1 (Inference) and Lab 3 (Orchestration).

## Technical Configuration
- **Endpoint:** `http://localhost:6333`
- **Collection Name:** `portfolio_memory`
- **Distance Metric:** Cosine Similarity (Optimal for modern embedding models).

## Setup
1. Navigate to `labs/lab2-rag/`
2. Run `docker compose up -d`
3. Verify via Dashboard: `http://localhost:6333/dashboard`
