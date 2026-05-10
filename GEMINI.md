# Personal AI Assistant (Raspberry Pi 5)

This project aims to create a hybrid AI assistant running locally on a Raspberry Pi 5 (16GB RAM, NVMe SSD) using Gemma 2 and integrating with Gemini CLI for complex tasks.

## Architecture

1.  **Local LLM Engine:** Ollama (running Gemma 2 9B).
2.  **Web Interface:** Open WebUI (running in Docker).
3.  **Hybrid Integration:** Gemini CLI configured to route simple tasks to Ollama and complex tasks to Gemini (1.5 Pro/Flash).
4.  **Remote Access:** Cloudflare Tunnel for secure access via a custom domain.
5.  **Repository:** Hosted on GitHub and mirrored in `/home/max/Documents/projects/personal-ai-assistant`.

## Setup Steps

### 1. Local Model Setup (Ollama)
- [ ] Install Ollama.
- [ ] Pull Gemma 2 9B model.
- [ ] Verify performance on RPi 5.

### 2. Web Interface (Open WebUI)
- [ ] Set up `docker-compose.yml` for Open WebUI.
- [ ] Connect Open WebUI to the local Ollama instance.

### 3. Hybrid Gemini CLI Configuration
- [ ] Define routing logic for "simple" vs "complex" tasks.
- [ ] Configure Gemini CLI to use the local Ollama API for local tasks.

### 4. Deployment & Security
- [ ] Set up Cloudflare Tunnel (cloudflared).
- [ ] Configure Cloudflare Zero Trust for authentication.
- [ ] Push to GitHub.

## Project Notes
- **Hardware:** Raspberry Pi 5, 16GB RAM, Intenso M.2 SSD PCIe Premium.
- **Model Recommendation:** Gemma 2 9B is the sweet spot for 16GB RAM.
