<div align="center">

# 🧠 AlperNab

### Infrastructure UX for provider routing, tools, cost, billing, artifacts, and platform-level operations.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?logo=fastapi&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-Job_History-003B57?logo=sqlite&logoColor=white) ![Local LLM](https://img.shields.io/badge/Local_LLM-Ollama%20%7C%20LM%20Studio%20%7C%20vLLM-111827) ![Cloud LLM](https://img.shields.io/badge/Cloud_LLM-OpenAI%20%7C%20Anthropic%20%7C%20Gemini%20%7C%20Mistral-7C3AED) ![No Fake Data](https://img.shields.io/badge/Policy-No_Fake_Live_Data-red)

**Domain:** `General AI Utility` · **Suite:** `AI Platform Core` · **Accent:** `#818cf8`

[🚀 Quick Start](#-quick-start) · [✨ Features](#-features) · [🎛️ Customization](#️-customization) · [🧠 LLM Providers](#-llm-providers) · [🧪 Testing](#-testing) · [🧯 Troubleshooting](#-troubleshooting)

</div>

---

## 🧭 What This Project Does

**AlperNab** is a standalone, browser-based AI workflow app for **General AI Utility**. It turns structured inputs, uploaded files, and project-specific settings into reviewable outputs using a deterministic local engine plus optional local/cloud LLM enhancement.

**Core job:** Personal AI builder profile and standalone platform workspace.

**Designed for:** Visitors, collaborators, clients, and operators who want to understand and run the AlperNab AI project workspace.

**Why use it:**

- 🧩 **Standalone project folder:** run this project by itself without depending on a central dashboard.
- 🖥️ **Elegant GUI:** includes project-specific panels, structured forms, upload handling, output preview, and exports.
- 🧠 **Model-flexible:** choose local models for privacy or cloud models for stronger reasoning.
- 🧾 **Auditable:** every run is stored in SQLite with inputs, settings, result, and export history.
- 🚫 **No fake live data:** external systems are only used when real API keys/connectors are configured.
- 🛡️ **Human review gates:** sensitive legal, medical, hiring, finance, or security outputs are flagged for review.

---

## ✨ Features

- domain-aware analysis
- structured output
- validation
- export
- human review

### 🧱 Built-In Platform Capabilities

- ⚡ **FastAPI backend** with documented JSON endpoints.
- 🎨 **Responsive web UI** with dark, polished SaaS-style layout.
- 📁 **File upload and text extraction** for common document/code formats.
- 🗂️ **Job history** saved locally in `data/*.sqlite3`.
- 🔐 **Encrypted provider settings** for API keys and local endpoints.
- 📤 **Exports** to Markdown, JSON, DOCX, and PDF when dependencies are available.
- 🔌 **Provider routing** for local and cloud LLMs.
- 🧪 **Local test file** to verify the project runs.

---

## 🎨 UX/UI Design

**UX profile:** `AI Platform Control Plane`

**Workflow layout:** Provider/tool intake → routing/security → execution → audit/export

**Empty state:** Configure local/cloud providers or paste a platform workflow. No provider keys are required for Rule Engine mode.

### Main UI Components

- Profile README preview
- Project portfolio table
- Stack badges panel
- Collaboration CTA
- Deployment checklist

### Review / Workflow Lanes

- Configure
- Route
- Execute
- Audit
- Optimize

### Metrics Shown in the Interface

- Provider readiness
- Cost control
- Security posture
- Execution reliability

### Quick Actions

- Review profile README
- Generate project summary
- Check links/badges
- Prepare GitHub profile update

---

## 🧩 Project Inputs

These are the main fields exposed by the GUI and `/api/run`. Required fields are enforced before execution.

| Field | Type | Required | Default | Purpose |
|---|---:|:---:|---|---|
| `div_align_center`<br><div align="center"> | text | Yes | — | Affects input: <div align="center">. |
| `work_brief`<br>Work brief / source text / URL / instructions | textarea | Yes | — | Paste the material, URL, description, or instruction needed for this project. |

---

## 🎛️ Customization

This project is not a generic prompt box. The customization controls are connected to workflow behavior, validation, output shape, and export format.

| Field | Type | Required | Default | Purpose |
|---|---:|:---:|---|---|
| `execution_mode`<br>Execution mode | select | No | Production | Controls strictness, depth, and output format for this project workflow. |
| `language`<br>language | select | No | English | Affects customization: language. |
| `output_format`<br>output format | select | No | Markdown | Affects customization: output format. |
| `strictness`<br>strictness | slider | No | 50 | Affects customization: strictness. |
| `privacy_mode`<br>privacy mode | select | No | cloud allowed | Affects customization: privacy mode. |
| `confidence_threshold`<br>confidence threshold | slider | No | 50 | Affects customization: confidence threshold. |

### Select / Option Controls

- **Execution mode**: Draft, Production, Audit / strict review, JSON/API output
- **language**: English, Arabic, Egyptian Arabic, French, German, Spanish
- **output format**: Markdown, JSON, CSV, PDF, DOCX, XLSX
- **privacy mode**: cloud allowed, local only, redact sensitive data

---

## 🧠 LLM Providers

You can run the project with the local deterministic engine, or enhance the output with a configured LLM provider.

### Supported Provider Types

| Provider Type | Examples | Best For |
|---|---|---|
| Local OpenAI-compatible | Ollama, LM Studio, vLLM | Private files, offline/local workflows, cost control |
| Cloud OpenAI-compatible | OpenAI, OpenRouter, custom gateway | General high-quality generation and structured output |
| Anthropic | Claude models | Long-context reasoning and document-heavy workflows |
| Google Gemini | Gemini models | Multimodal or Google ecosystem workflows |
| Mistral | Mistral API | Fast European cloud models |
| Azure OpenAI | Azure deployments | Enterprise-controlled cloud deployment |
| AWS Bedrock | Bedrock-hosted models | AWS enterprise environments |

### Recommended Model Usage

| Use Case | Recommendation |
|---|---|
| Drafting | fast cloud or local instruct model |
| Reasoning | strong reasoning model |
| Private documents | local model via Ollama/LM Studio/vLLM |
| Vision/PDF pages | vision-capable model when image pages are used |

---

## 🚀 Quick Start

### 1) Clone or open this folder

```bash
cd AlperNab
```

### 2) Run on macOS / Linux / WSL

```bash
chmod +x run_gui.sh
./run_gui.sh
```

### 3) Run on Windows PowerShell

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\run_gui_windows.ps1
```

### 4) Open the GUI

```text
http://127.0.0.1:9101
```

---

## 🛠️ Manual Installation

Use this when you want full control instead of the run scripts.

```bash
cd AlperNab
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
cp .env.example .env           # Windows: copy .env.example .env
uvicorn app.main:app --host 127.0.0.1 --port 9101
```

---

## 🔐 Environment Variables

The project can be configured through the GUI settings screen or `.env`/environment variables.

| Variable | Purpose |
|---|---|
| `AI_SUITE_HOST` | Host to bind the local app, usually `127.0.0.1`. |
| `AI_SUITE_PORT` | Port for this project GUI, default `9101`. |
| `AI_SUITE_DB` | SQLite database path for job history. |
| `AI_SUITE_SECRET_KEY` | Secret used for local encryption/signing. Set this in production. |
| `OPENAI_API_KEY` | Enables OpenAI-compatible cloud calls. |
| `ANTHROPIC_API_KEY` | Enables Anthropic/Claude calls. |
| `GEMINI_API_KEY` | Enables Google Gemini calls. |
| `OPENROUTER_API_KEY` | Enables OpenRouter model routing. |
| `MISTRAL_API_KEY` | Enables Mistral cloud models. |
| `AZURE_OPENAI_ENDPOINT` | Azure OpenAI endpoint URL. |
| `AZURE_OPENAI_API_KEY` | Azure OpenAI key. |
| `AZURE_OPENAI_DEPLOYMENT` | Azure deployment name. |
| `OLLAMA_BASE_URL` | Local Ollama OpenAI-compatible base URL. |
| `LMSTUDIO_BASE_URL` | Local LM Studio OpenAI-compatible base URL. |
| `VLLM_BASE_URL` | Local vLLM OpenAI-compatible base URL. |

---

## 🖥️ How to Use the GUI

1. Open the local URL.
2. Review the project purpose and workflow lanes.
3. Fill the required input fields.
4. Adjust only the project-related customization controls.
5. Upload source files when needed.
6. Choose `Rule Engine` for local deterministic output or select a configured LLM provider.
7. Run the workflow.
8. Review warnings, scorecards, and output sections.
9. Export the result as Markdown, JSON, DOCX, or PDF.

---

## 🔄 Workflow

- <div align="center">

### Analysis Modules

- repo_readme_analyzer
- project_inventory
- action_tracker

### Output Sections

- Project summary
- Detected purpose
- Missing setup
- Next actions

### Scorecards

- Input completeness
- Domain fit
- Risk level
- Automation readiness
- Export readiness

---

## 📤 Outputs & Exports

- Markdown report
- JSON result
- CSV table
- PDF report

The export system is designed for reviewable deliverables. For regulated or business-critical work, export drafts should be reviewed before sending to clients, customers, patients, employees, authorities, or production systems.

---

## 🔌 Real Integrations & Connector Policy

Configured integrations in this standalone folder:

- File upload
- REST API
- Export download
- Job history

### Real Connector Requirements

- approved legal playbook or clause library
- jurisdiction-specific review by qualified counsel
- document management/e-sign connector if exporting final agreements

**Important:** this project does not simulate live data. If a workflow needs live Shopify, ATS, ERP, tax, customs, medical, security, market, map, analytics, or repository data, it must be connected with valid credentials and real API access. Missing connectors should produce clear setup errors rather than invented results.

---

## 🧯 Guardrails

- Show uncertainty and confidence
- Cite evidence from input when possible
- Human review required for legal, medical, financial, hiring, or security decisions
- Do not invent facts absent from input

Recommended operating rules:

- ✅ Use local models for private or sensitive files.
- ✅ Keep API keys out of Git.
- ✅ Review low-confidence or high-impact outputs manually.
- ✅ Keep source files and exported deliverables organized under `data/`.
- ❌ Do not treat AI output as legal, medical, tax, hiring, trading, or security authority without expert review.

---

## 🧪 Testing

Run the local smoke test:

```bash
python tests/test_single_project.py
```

Run a health check after starting the server:

```bash
curl http://127.0.0.1:9101/api/health
```

Expected result: the API returns `ok: true` and identifies this project.

---

## 🧬 API Usage

| Method | Endpoint | Use |
|---|---|---|
| `GET` | `/` | Opens the browser GUI. |
| `GET` | `/api/health` | Health check for deployment and uptime monitoring. |
| `GET` | `/api/projects` | Returns the local project configuration. |
| `GET` | `/api/projects/{slug}` | Returns the project plugin metadata. |
| `GET` | `/api/providers` | Lists configured providers and local/cloud options. |
| `POST` | `/api/providers` | Saves provider settings/API keys. |
| `POST` | `/api/upload` | Uploads source files for extraction or context. |
| `POST` | `/api/run` | Runs the project workflow. |
| `GET` | `/api/jobs` | Lists previous runs and job history. |
| `GET` | `/api/jobs/{job_id}` | Reads one completed job. |
| `GET` | `/api/jobs/{job_id}/export/{fmt}` | Exports a job as `md`, `json`, `docx`, or `pdf`. |
| `GET` | `/api/project-local-status` | Verifies local project registration and implementation status. |

### Minimal Run Request

```bash
curl -X POST http://127.0.0.1:9101/api/run \
  -H "Content-Type: application/json" \
  -d '{
    "inputs": {
      "work_brief": "Paste the source material or task details here"
    },
    "customization": {
      "execution_mode": "Production"
    },
    "provider": "rule_engine"
  }'
```

---

## 📁 Folder Structure

```text
AlperNab/
├─ app/                         # FastAPI backend, schemas, DB, providers, exports
├─ static/                      # Browser GUI assets
├─ plugins/                     # Project plugin JSON metadata
├─ data/                        # SQLite DB, uploads, exports
├─ tests/                       # Smoke tests
├─ project_config.json          # Project-specific inputs, controls, UX, workflow
├─ PROJECT_IMPLEMENTATION.md    # Implementation details and domain notes
├─ requirements.txt             # Python dependencies
├─ run_gui.sh                   # macOS/Linux/WSL launcher
├─ run_gui_windows.ps1          # Windows PowerShell launcher
└─ README.md                    # This file
```

---

## 🚢 Deployment Notes

For local/private deployment, run with `uvicorn` behind a reverse proxy if needed. For production:

- Set `AI_SUITE_SECRET_KEY`.
- Use HTTPS.
- Store provider keys in environment variables or a proper secret manager.
- Restrict upload sizes and allowed file types.
- Back up the SQLite database or move job storage to a managed database.
- Add authentication before exposing beyond localhost.
- Enable logging and monitoring.

Example production-style command:

```bash
AI_SUITE_HOST=0.0.0.0 AI_SUITE_PORT=9101 uvicorn app.main:app --host 0.0.0.0 --port 9101
```

---

## 🧯 Troubleshooting

| Problem | Fix |
|---|---|
| `python` not found | Install Python 3.10+ and ensure it is on PATH. |
| PowerShell blocks the script | Run `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`. |
| Port already in use | Set another port: `AI_SUITE_PORT=9200 ./run_gui.sh`. |
| Provider fails | Verify API key, base URL, selected model, and account quota. |
| Local model fails | Start Ollama/LM Studio/vLLM before running the workflow. |
| PDF/DOCX export fails | Reinstall requirements and confirm optional export dependencies installed. |
| Upload extraction is incomplete | Use cleaner source files or paste the important text into `work_brief`. |

---

## 🧭 Extension Points

You can extend this project by editing:

- `project_config.json` for inputs, settings, output sections, UX metadata, and workflow labels.
- `plugins/AlperNab.json` for plugin metadata.
- `app/domain_engine.py` for deterministic business logic.
- `app/llm_gateway.py` for provider integrations.
- `static/app.js` and `static/styles.css` for GUI behavior and component design.
- `tests/test_single_project.py` for stronger project-specific tests.

---

## ✅ Final Implementation Status

| Area | Status |
|---|---|
| Standalone folder GUI | ✅ Implemented |
| FastAPI backend | ✅ Implemented |
| Project-specific config | ✅ Implemented |
| Local deterministic workflow | ✅ Implemented |
| Local/cloud LLM routing | ✅ Implemented |
| Uploads and exports | ✅ Implemented |
| Job history | ✅ Implemented |
| Real external connectors | ⚠️ Requires valid credentials/API setup |
| Fake/simulated live data | ❌ Not allowed |

---

## 📜 License

Use the license included in this folder. If no explicit license is present, treat the code as private until you choose one.


---

## 👤 Original AlperNab Profile README

The profile README content you attached is preserved below so the standalone GUI documentation and your public GitHub profile content live together in this folder.

<div align="center">

<img src="https://avatars.githubusercontent.com/u/63242650?v=4" width="96" style="border-radius:50%"/>

# Alper Nabil Gabra Zakher

**AI Builder · SaaS · E-commerce Automation · Fintech**

I build AI-powered products, autonomous e-commerce systems, and open-source developer tools that solve real business problems.  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-alper--nabil-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/alper-nabil)
[![Website](https://img.shields.io/badge/Website-alpernabil.com-000?style=flat&logo=safari&logoColor=white)](https://www.alpernabil.com)
[![Linktree](https://img.shields.io/badge/Linktree-its.alper-39E09B?style=flat&logo=linktree&logoColor=white)](https://linktr.ee/its.alper)
[![Trailblazer](https://img.shields.io/badge/Trailblazer-alpern-00A1E0?style=flat&logo=salesforce&logoColor=white)](https://trailblazer.me/id/alpern)

</div>

---

## 🚀 What I'm Building

| Project | What it is | Stack |
|--------|-----------|-------|
| **[shopify-mcp-server](https://github.com/AlperNab/shopify-mcp-server)** | MCP server — let Claude Code manage your Shopify store | TypeScript · MCP SDK |
| **[llm-billing-engine](https://github.com/AlperNab/llm-billing-engine)** | Drop-in token credit system for AI SaaS — reserve, settle, audit | Python · PostgreSQL |
| **[universal-doc-parser](https://github.com/AlperNab/universal-doc-parser)** | Any financial PDF → clean structured JSON via Claude vision | Python · Claude API |
| **[gemini-audio-transcriber](https://github.com/AlperNab/gemini-audio-transcriber)** | Gemini 2.5 audio transcription library with diarization | Python · Gemini API |
| **[launch-kit](https://github.com/AlperNab/launch-kit)** | README → full launch marketing package (HN, PH, Reddit, Twitter) | Python · Claude API |

---

## 🛠️ Stack

**AI / ML**
![Claude](https://img.shields.io/badge/Claude_API-D97757?style=flat&logo=anthropic&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_2.5-4285F4?style=flat&logo=google&logoColor=white)
![RunPod](https://img.shields.io/badge/RunPod-673AB7?style=flat)

**Backend**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)

**E-commerce**
![Shopify](https://img.shields.io/badge/Shopify-96BF48?style=flat&logo=shopify&logoColor=white)
![Klaviyo](https://img.shields.io/badge/Klaviyo-000?style=flat)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat&logo=graphql&logoColor=white)

---

## 📊 Stats

<div align="center">
<img height="155" src="https://github-readme-stats.vercel.app/api?username=AlperNab&show_icons=true&theme=default&hide_border=true&count_private=true"/>
<img height="155" src="https://github-readme-stats.vercel.app/api/top-langs/?username=AlperNab&layout=compact&theme=default&hide_border=true&langs_count=8"/>
</div>

---

<div align="center">
<sub>Open to collaborations on AI tooling · <a href="https://linkedin.com/in/alper-nabil">DM on LinkedIn</a></sub>
</div>
