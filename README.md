# Ari Harrison

**Founder, NovoMCP · The open computational chemistry engine for drug discovery and materials science.**

The interesting problem isn't getting a model to say something. It's building the system around the model so its output can be acted on: safely, correctly, repeatedly, with a record of what happened.

## Now

- Building: **NovoMCP** — the open computational chemistry engine. Open-sourced July 2026 under Apache-2.0, shipped through **v1.4.3**. MCP + REST, 69 tools. Clone it and it boots with zero external services — no auth, no account, no API key. Self-host it, or have NovoMCP set it up on your infrastructure under a branded subdomain. Solo founder.
- Shipped: **[Novo Station](https://novomcp.com/novo-station)** — the NovoMCP compute core on NVIDIA DGX Spark, one GB10 desktop system from one compose file. About 0.4× a datacenter L40S's raw MD speed, 1.2–1.5× its throughput per watt. [Field report](https://www.novomcp.com/news/what-actually-breaks-when-you-port-a-chemistry-stack-to-dgx-spark).
- Open to: **product, AI, and 0-to-1 leadership conversations.** Bay Area or remote. Particularly interested in production AI systems, MCP-shaped infrastructure, and applied AI at companies where correctness matters.
- Contact: ariharrisonlab@gmail.com · [LinkedIn](https://www.linkedin.com/in/ariharrisonlab/)
- Backed by: NVIDIA Inception · AWS Activate · Microsoft Founders Hub

## One Engine, Many Surfaces

The engine is the product. The surface is how you reach it. Each surface is a thin, backend-configurable client — point it at a local engine (default) or a hosted one (with a key).

- **MCP**: The chat surface, one endpoint on the open engine (`localhost:8018/mcp`). The hosted Novo + Novo Compute servers were retired at the open-source launch. [Engine](https://novomcp.com/engine) · [Novo Compute](https://novomcp.com/novo-compute)
- **REST API**: ships in the open engine (`localhost:8018`). Single endpoint shape (`POST /v1/tools/{name}`), OpenAPI 3.1 catalog. `api.novomcp.com` hosts the two closed services, FAVES and FEP; hosted billing was retired with the open-source release. [API docs](https://novomcp.com/api)
- **NovoWorkbench**: The workstation. Native desktop (macOS + Windows), local RDKit + offline alert screening, bring-your-own-LLM. Design-partner preview; ships as OSS in v1.5.x.
- **Chrome extension**: Hover any SMILES for ADMET / FAVES. Ships as a [sideload](https://github.com/NovoMCP/novomcp-chrome-sideload) pointed at your own engine.
- **Word add-in**: Inline SMILES profiling in manuscripts and grants. Private beta.
- **Bundled dashboard**: A minimal Next.js dashboard shipped inside the OSS repo (`frontend-nextjs/`) — auth, keys, usage, pipeline jobs. Runs on localhost when you self-host; on the branded subdomain when NovoMCP sets it up.

## Also shipping · Open source

- **[novomcp-lite](https://github.com/NovoMCP/novomcp-lite)** (Apache-2.0). A lightweight, standalone version of NovoMCP's cheminformatics — for when you just want the wrappers, not the whole engine. `pip install novomcp-lite` — eight zero-config tools (RDKit properties, profiling, synthetic-accessibility scoring, PAINS/BRENK alerts, library screening + ChEMBL / ClinicalTrials.gov / bioRxiv search), as a Python library or an MCP server. It's the same code the full engine runs on, so the numbers match — just without the rest of the engine. Prompted by user feedback; on PyPI (v0.1.1).
- **Open compute-service wrappers** (Apache-2.0). The engine's GPU services ship as standalone repos, each deployable on its own: [gromacs-md](https://github.com/NovoMCP/gromacs-md) (GROMACS MD), [novomcp-nnp](https://github.com/NovoMCP/novomcp-nnp) (neural-network potentials), [novomcp-qm](https://github.com/NovoMCP/novomcp-qm) (quantum chemistry).
- **[NovoMD](https://github.com/ariharrisonlab/NovoMD)** (MIT). Local-first molecular descriptors. SMILES → 32+ descriptors from a 3D conformer, calculated on your own machine, no account. Ships as Python library (`pip install novomd`) + CLI (`novomd props "CCO"`) + [Hugging Face MCP endpoint](https://huggingface.co/spaces/quantnexusai/novomd) (works with Claude, Cursor, any MCP client) + Docker REST service. The design call: scope discipline. No ADMET, no pKa, no binding. Documented in the README and shipped as an agent skill.

See the [full product portfolio →](https://ariharrisonlab.github.io/portfolio.html)

## The Stack

- **The Engine**: MCP + REST, 69 tools, 14 always-available on a fresh clone (now v1.4.3)
- **Desktop GPU**: [Novo Station](https://novomcp.com/novo-station), the compute core on NVIDIA DGX Spark (GB10)
- **Runs local**: boots with zero external services — no auth, no account, no API key; audit to `~/.novo/audit.jsonl`
- **Pluggable spine**: auth / metering / audit swap local ↔ hosted ↔ custom by env flag — same code standalone or operated, no OSS/enterprise fork
- **Wraps open compute**: RDKit · GROMACS · AutoDock-GPU · OpenFold · Boltz · Gnina · xTB · ANI-2x · AIMNet2 · MACE; ALCHEMI-accelerated engine axis across geometry, energy, and conformer search (through v1.3.0); in-process cheminformatics sourced from the open novomcp-lite package (v1.4.0)
- **License**: Apache-2.0 top-level (orchestration core BSL 1.1 → Apache 2029-07-12)
- **Compliance**: FAVES V4 (hosted certified API) — 8 jurisdictions, 1,585 structural alerts
- **Verticals**: Drug discovery + materials science

## Ecosystem

NVIDIA Inception · AWS Activate · Microsoft Founders Hub

## Links

- [Product portfolio (one engine, its surfaces)](https://ariharrisonlab.github.io/portfolio.html)
- [NovoMCP](https://novomcp.com) · [Repo](https://github.com/NovoMCP/novomcp) · [Docs](https://docs.novomcp.com/)
- [X / Twitter](https://x.com/ariharrisonlab)
- [Google Scholar](https://scholar.google.com/citations?hl=en&user=O3Bdfh8AAAAJ)
- [LinkedIn](https://www.linkedin.com/in/ariharrisonlab/)
- [GitHub](https://github.com/ariharrisonlab)
- [YouTube](https://www.youtube.com/@ariharrisonlab)
- [Writing](https://substack.com/@ariharrisonlab)

## Leadership decisions

A selection of product, infra, and positioning calls made shipping NovoMCP (full version at [ariharrisonlab.github.io/#leadership](https://ariharrisonlab.github.io/#leadership)).

- **Open the engine at v1.0**: Apache-2.0 top-level, BSL 1.1 → Apache 2029-07-12 for the core. The moat is FAVES certification + FEP + the deployment service, not the code or the open models.
- **Two MCP servers, not one**: governance separation between free-tier and paid-only tools
- **Scale-to-zero by default**: every compute service ships with `min_replicas=0`
- **"Engine" never "platform"**: locked public language to one positioning noun
- **Killed the autonomous-campaign system**: replaced with human-in-the-loop via MCP elicitation
- **Self-hosted or set up for you, no middle**: killed the credit-tier ladder at the OSS launch — free-forever self-host, or a deployment service on your infrastructure with certified FAVES
- **Private-endpoint-only infra**: build on GH-hosted runners, deploy via OIDC → SSM → bastion

---

*The system that makes the agent safe to deploy is the product.*
