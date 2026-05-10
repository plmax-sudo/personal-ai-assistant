# Personal AI Assistant (Raspberry Pi 5)

This project aims to create a local AI assistant running on a Raspberry Pi 5 (16GB RAM, NVMe SSD) using Gemma 4, with Open WebUI as the primary interface.

## Architecture

1.  **Local LLM Engine:** Ollama (running Gemma 4 E4B).
2.  **Web Interface:** Open WebUI (running in Docker).
3.  **Remote Access:** Cloudflare Tunnel for secure access via a custom domain (To be implemented by user).
4.  **Repository:** Hosted on GitHub and mirrored in `/home/max/Documents/projects/personal-ai-assistant`.

## Setup Steps

### 1. Local Model Setup (Ollama)
- [x] Install Ollama.
- [x] Pull Gemma 4 E4B model (`ollama pull gemma4:e4b`).
- [x] Verify performance on RPi 5 (Snappy performance achieved).

### 2. Web Interface (Open WebUI)
- [x] Set up `docker-compose.yml` for Open WebUI.
- [x] Connect Open WebUI to the local Ollama instance.
- [x] Verify local access at `http://localhost:3000`.

### 3. Web Search Integration (SearXNG)
- [x] Deploy SearXNG container.
- [x] Configure `settings.yml` to allow JSON output.
- [ ] Connect Open WebUI to SearXNG (User task in Admin Panel).

## Backlog / Future Tasks
- [ ] **Hybrid Gemini CLI Integration:** Configure routing logic to use local Gemma 4 for simple tasks and Gemini 3/3.1 Cloud for complex reasoning.
- [ ] **Cloudflare Tunnel:** Secure the local instance for remote access.
- [ ] **Personal Assistant Persona:** Build out custom system prompts and knowledge base in Open WebUI.

## Project Notes
- **Hardware:** Raspberry Pi 5, 16GB RAM, Intenso M.2 SSD PCIe Premium.
- **Model Recommendation:** **Gemma 4 E4B**. This model provides the best balance of speed and intelligence for the Raspberry Pi 5, ensuring a "snappy" user experience. The 26B MoE model was removed as it was too slow for real-time assistant use.
