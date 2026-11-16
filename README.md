# Voice Agent Platform

Open-source voice agent platform with a built-in simulation lab. Built on [Pipecat](https://docs.pipecat.ai).

Pipeline: browser mic → Deepgram (speech-to-text) → OpenAI (LLM) → Cartesia (text-to-speech) → speaker.

## Run it locally (Windows)

1. Install uv (PowerShell):
   ```powershell
   powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
   ```
2. Get API keys (all have free credits):
   - Deepgram: https://console.deepgram.com
   - OpenAI: https://platform.openai.com/api-keys
   - Cartesia: https://play.cartesia.ai/keys
3. Add keys:
   ```powershell
   cd server
   copy .env.example .env
   notepad .env
   ```
4. Install and run:
   ```powershell
   uv sync
   uv run bot.py -t webrtc
   ```
5. Open http://localhost:7860, click Connect, allow the mic, and talk.

First run takes ~20 seconds while models download.

## Status

See the tracker doc for milestones.
