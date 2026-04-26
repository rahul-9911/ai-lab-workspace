# Lab 4: Multimodal Analysis (Vision)

This lab unlocks the "Senses" of the AI Home Lab, utilizing the native trimodal capabilities of **Gemma 4:E2B**.

## Capabilities
- **Native Vision Processing:** Unlike older architectures that required a separate CLIP or ViT model, Gemma 4 processes image tokens natively within the same reasoning engine.
- **Image-to-Reasoning:** The agent can "see" an image and apply its thinking mode to decompose the visual elements before responding.
- **Zero-Config Multimodal:** The n8n orchestrator automatically routes binary chat attachments to the Ollama inference engine.

## Use Cases Demonstrated
1.  **Visual Description:** Accurately describing scene contents, colors, and layout.
2.  **Contextual Logic:** Applying reasoning to visual data (e.g., "Analyze this screenshot for errors").
3.  **Cross-Modal Synthesis:** Using visual inputs to inform text-based decisions.

## Setup
1. Ensure Lab 1 (Ollama) is running with `gemma4:e2b`.
2. In the n8n Chat Trigger, enable **Attachments**.
3. Upload an image and ask: "Describe this image in detail."
