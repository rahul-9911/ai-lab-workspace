# Lab 5: Parameter-Efficient Fine-Tuning (LoRA)

This capstone lab demonstrates how to specialize a general-purpose model for a specific technical domain using **LoRA (Low-Rank Adaptation)**.

## Technical Highlights
- **Base Model:** Gemma 4 (2.3B Trimodal Architecture)
- **Framework:** **Unsloth** (Optimized for 2026 hardware acceleration)
- **Memory Efficiency:** Utilized 4-bit quantization and PEFT (Parameter-Efficient Fine-Tuning) to train on a single 12GB NVIDIA GPU.
- **Optimization:** Achieved a ~0.16% trainable parameter count (8.1M params), allowing for rapid specialization without the cost of full fine-tuning.

## Training Workflow
1.  **Environment:** Containerized Jupyter environment with CUDA/Unsloth optimization.
2.  **Dataset:** Custom JSONL dataset formatted with context-instruction-response triplets.
3.  **Kernel Shortcuts:** Used Unsloth's hand-written kernels to reduce VRAM usage by 70%.
4.  **Export:** Saved the LoRA adapter for deployment in Ollama or other inference engines.

## Key Learning
Demonstrated the ability to handle "bleeding-edge" architecture conflicts between Trimodal Processors and Text-based Tokenizers—a common challenge in early 2026 AI engineering.
