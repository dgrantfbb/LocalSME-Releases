# Local SME

RAG-powered knowledge Q&A with citations — on your machine.

Ingest docs and sites into a local knowledge base, ask grounded questions with `[#n]` citations, and when the model is stuck export a **shareable handoff file**, get a human answer offline, then import it back (optionally into the KB).

**[Download the latest installer →](https://github.com/dgrantfbb/LocalSME-Releases/releases/latest)**

> **Source code is not published here.** This repository hosts installers, release notes, and product docs only.

---

## What you get

- **Local-first RAG** — SQLite + vectors under your user data; your files stay on your machine
- **Citations** — answers ground in retrieved chunks with source links
- **Handoff** — export a pack when the AI fails; import the human resolution and optionally learn from it
- **Your LLM** — OpenAI-compatible chat hosts (Ollama / LM Studio / Bionic and similar)
- **Embeddings** — built-in local `nomic-embed-text-v1.5` (CPU) or a remote embed host

---

## How to use

1. **Install** — download the latest Windows installer from [Releases](#download).
2. **Configure chat** — Settings → point at your OpenAI-compatible LLM host and model.
3. **Set up embeddings** — download the built-in ONNX model into the app’s models folder (or use a remote embed preset).
4. **Build a knowledge base** — add Markdown/docs, optional GitHub repos, or crawl a public site.
5. **Ask** — chat with citations; export a handoff pack when confidence is low.

---

## Agent Host (MCP / HTTP)

Local SME can expose a **loopback** Agent Host so Cursor or other tools use your KBs as RAG without the UI (HTTP on localhost, or MCP stdio). Enable and copy the config snippet from **Settings → Agent Host** in the installed app. The MCP server ships with the toolkit/source — not with this releases repository.

| | |
|---|---|
| **On your machine** | Loopback only — no cloud builder for your KB |
| **Private by design** | Your data and keys stay local |
| **Agent as partner** | Search and ask against your indexed sources |

---

## Download

See [Releases](https://github.com/dgrantfbb/LocalSME-Releases/releases/latest) for the latest installer.

## System requirements

- Windows 10/11 (64-bit) for `.exe` builds
- A local or reachable OpenAI-compatible LLM for chat
- Optional: quantized ONNX files for built-in embeddings (not bundled in the installer)

## Updates

Packaged installs check for updates automatically (and via Settings → **Updates**) against this repository’s GitHub Releases feed (`latest.yml`).

You can always download and run the latest installer from [Releases](https://github.com/dgrantfbb/LocalSME-Releases/releases/latest) as a fallback.

## License

MIT — see [LICENSE](LICENSE).
