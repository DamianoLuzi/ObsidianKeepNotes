
# Free "Jarvis" on Your Mac — Optimized Setup Guide

**Target:** MacBook Air M3, 24 GB · **Cost:** $0 in tooling · **Goal:** an assistant that reads your notes/photos _and does tasks_, from CLI or app.

## The one principle that makes it work

Separate the two things everyone conflates:

- **Brain** = the model (local Ollama, or a cloud sub you already pay for).
- **Harness** = the runtime giving it memory, tools, a plan→act→verify loop, scheduling. **This is the Jarvis part.** Claude Code and I (MeshClaw) are harnesses, not models.

Your Ollama note nails the _brain_ — it just stops one layer short. This guide adds the harness (**Goose**) on top.

code

```
        You (CLI · desktop app · scheduled job)
                      │
                GOOSE (harness)  ← the Jarvis layer
         ┌────────────┼─────────────┐
      Models        Tools         Memory
    (Ollama +     (MCP: files,   (memory
     cloud sub)    browser, git)  extension)
```

## Phase 0 — Prereqs (5 min)

bash

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
xcode-select --install
```

## Phase 1 — Local brain: Ollama (20 min)

bash

```bash
brew install ollama
brew services start ollama          # API on 127.0.0.1:11434, auto-starts on login

ollama pull qwen2.5-coder:14b       # coding / agent reasoning — 24GB sweet spot
ollama pull qwen2.5vl               # vision: photos, screenshots, captions
ollama pull qwen2.5:7b              # fast general text / notes / strategy
ollama pull nomic-embed-text        # embeddings for memory / "talk to my notes"
```

On 24 GB you can run a 14B coder (agent loops need the reasoning headroom) _alongside_ a 7B vision model. 32B q4 fits but is slower — start at 14B.

## Phase 2 — Chat UI for content work (10 min)

Pick one:

- **Open WebUI** (most powerful — drag photos + paste notes in one chat):

bash

```bash
  pip install open-webui
  open-webui serve --host 127.0.0.1 --port 8080   # localhost only
  
```

- **LM Studio** — zero-terminal GUI, from lmstudio.ai.

## Phase 3 — The Jarvis layer: Goose ★ the real upgrade

Closest public equivalent to MeshClaw: local-first, CLI + desktop, native **MCP extensions**, **skills**, and **recipes**. Apache-2.0, free.

bash

```bash
curl -fsSL https://github.com/block/goose/releases/download/stable/download_cli.sh | bash
goose configure
```

**Hybrid routing (the key move):** default to **Ollama** (free/private) for photos/notes/files; add a strong model for hard loops via **ACP** using your existing Claude/ChatGPT sub (no extra cost), or a pennies-per-token key.

**Add tools first — this is when it stops being a chatbot:** in `goose configure` enable _Developer_ (files+shell), _Computer Controller_ (browser), _Memory_. Then:

bash

```bash
goose "organize my ~/Downloads folder by file type and report what you moved"
```

> Google **retired Gemini CLI** (→ Antigravity) — don't build on it. Want coding-only instead of general Goose? Use **OpenCode** (the MIT open Claude Code clone) or **Aider**.

## Phase 4 — Content recipes (your use case)

bash

```bash
ollama run qwen2.5vl "3 Instagram captions, different tones: ./photo.jpg"
# batch a whole folder → Markdown:
for img in ~/Photos/switzerland/*.jpg; do
  echo "## $(basename "$img")" >> captions.md
  ollama run qwen2.5vl "one punchy caption + 3 hashtags: $img" >> captions.md
done
```

Then wrap it as a Goose **recipe** (`content.yaml`) and run headless: `goose run --recipe content.yaml`.

## Phase 5 — MeshClaw-style automation (launchd)

Schedule any recipe (this rebuilds my crons for free). `~/Library/LaunchAgents/com.jarvis.captions.plist` runs `goose run --recipe …` daily at 9:00; `launchctl load` it. (Full plist is in the saved artifact.)

## Model cheat-sheet (24 GB)

|Need|Model|
|---|---|
|Coding / agent loops|`qwen2.5-coder:14b`|
|Vision|`qwen2.5vl` (7B)|
|Fast text / notes|`qwen2.5:7b`|
|Memory / RAG|`nomic-embed-text`|
|Hard reasoning|Claude/ChatGPT via ACP (your sub)|

## Skip these (anti-patterns)

- ❌ Hand-building a custom `jarvis/` folder — Goose already _is_ that, tested.
- ❌ Days of RAG pipelines before the agent touches a file. Tools first.
- ❌ Expecting a local 7–14B to match Claude/GPT on 20-step loops. It won't — that's why hybrid exists.

## Reality check + cost

Agentic loops are much harder than chat; local models shine on private/simple/content work, frontier models still win on hard planning/debugging. Hybrid (Ollama for the cheap 90%, cloud for the hard 10%) is the sweet spot, and Goose toggles per task. **Total tooling cost: $0** — the only optional spend is a hard-reasoning model, and that's free if you route through a sub you already have.

**Weekend plan:** Day 1 → Phases 1–2. Day 2 → Phase 3 (get Goose editing files). Day 3 → Phases 4–5 (one recipe, scheduled). By Sunday: a scheduled, file-touching assistant.

---

Want me to go further? I can actually start executing this on your laptop (I'd verify Ollama's already here from your MeshClaw setup and pull the models), or tailor it more.