# Multi-Agent Surfing School Booking System with Background Observer Agent

Lightweight Python project providing several conversational agent modules (intake, billing, frontdesk, scheduler, observer, gear) and supporting prompts, tasks, and tools.

**Repository layout**
- `agent.py`: project entrypoint / runner
- `agents/`: agent implementations
- `prompts/`: YAML prompts used by agents
- `tasks/`: small task modules (name, age, email, etc.)
- `tools/`: integration helpers (calendar, payment, tide)
- `utils.py`, `requirements.txt`, `.env`, `venv/`

**Prerequisites**
- Python 3.10+ (3.12 tested in this workspace)
- Git

**Installation (local/dev)**
1. Create a virtual environment (recommended):
```
python -m venv venv
source venv/bin/activate
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Create a `.env` file at the repository root and add any required environment variables (API keys, database URLs, etc.). Example:
```
# .env
# OpenAI (LLM)
OPENAI_API_KEY=your_openai_api_key_here

# LiveKit (real-time / audio-video)
LIVEKIT_API_KEY=your_livekit_api_key_here
LIVEKIT_API_SECRET=your_livekit_api_secret_here
LIVEKIT_API_URL=https://your-livekit-instance.example.com

# Optional integrations
DATABASE_URL=postgres://user:pass@localhost:5432/dbname
PAYMENT_API_KEY=your_payment_provider_key
STRIPE_SECRET=your_stripe_secret

# Other secrets
OTHER_SECRET=...
```

**Run**
- Run the main entrypoint:
```
python agent.py
```

**Development notes**
- Virtual environment directory `venv/` and environment file `.env` are ignored by `.gitignore` to avoid leaking secrets and packages.



