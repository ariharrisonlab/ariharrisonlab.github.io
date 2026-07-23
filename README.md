# Ari Harrison

**Founder, NovoMCP · Shipping AI-native chemistry across six surfaces.**

The interesting problem isn't getting a model to say something. It's building the system around the model so its output can be acted on: safely, correctly, repeatedly, with a record of what happened.

## Now

- Building: **NovoMCP**. One computational chemistry engine, six surfaces. Solo founder, ~30 services in production on AWS.
- Open to: **product, AI, and 0-to-1 leadership conversations.** Bay Area or remote. Particularly interested in production AI systems, MCP-shaped infrastructure, and applied AI at companies where correctness matters.
- Contact: arimgianni@gmail.com · [LinkedIn](https://www.linkedin.com/in/ariharrisonlab/)
- Backed by: NVIDIA Inception · AWS Activate · Microsoft Founders Hub

## One Engine, Six Surfaces

The engine is the product. The surface is how you reach it.

- **MCP**: Novo + Novo Compute. The chat surface. [Novo](https://novomcp.com/novo) · [Novo Compute](https://novomcp.com/novo-compute)
- **REST API**: `api.novomcp.com`. Single endpoint shape, OpenAPI 3.1 catalog. [API docs](https://novomcp.com/api)
- **NovoWorkbench**: The workstation. One workbench, two runtimes (desktop + cloud). Same account across both.
- **Chrome extension**: Hover any SMILES for ADMET / FAVES. [Chrome Web Store](https://chromewebstore.google.com/detail/novomcp/nfnhfmfmaccidmepfhllcllnjopeonmf)
- **Word add-in**: Inline SMILES profiling in manuscripts and grants. Private beta.
- **Dashboard**: `app.novomcp.com`. The spine: auth, keys, billing, jobs. Where every surface authenticates.

## Also shipping · Open source

- **[NovoMD](https://github.com/ariharrisonlab/NovoMD)** (MIT). Local-first molecular descriptors. SMILES → 32+ descriptors from a 3D conformer, calculated on your own machine, no account. Ships as Python library (`pip install novomd`) + CLI (`novomd props "CCO"`) + [Hugging Face MCP endpoint](https://huggingface.co/spaces/quantnexusai/novomd) (works with Claude, Cursor, any MCP client) + Docker REST service. The design call: scope discipline. No ADMET, no pKa, no binding. Documented in the README and shipped as an agent skill.

See the [full product portfolio →](https://ariharrisonlab.github.io/portfolio.html)

## The Stack

- **The Engine**: 122M+ compounds, 100+ properties each, sub-50ms
- **Tool Catalog**: 69 tools across ADMET, FAVES, docking, MD, FEP, QM
- **Compliance**: FAVES V4, 8 jurisdictions, 1,585 structural alerts
- **Verticals**: Drug discovery + materials science
- **One account, one credit pool, one audit trail**: across all six surfaces

## Ecosystem

NVIDIA Inception · AWS Activate · Microsoft Founders Hub

## Links

- [Product portfolio (one engine, six surfaces)](https://ariharrisonlab.github.io/portfolio.html)
- [NovoMCP](https://novomcp.com)
- [X / Twitter](https://x.com/ariharrisonlab)
- [Google Scholar](https://scholar.google.com/citations?hl=en&user=O3Bdfh8AAAAJ)
- [LinkedIn](https://www.linkedin.com/in/ariharrisonlab/)
- [GitHub](https://github.com/ariharrisonlab)
- [YouTube](https://www.youtube.com/@ariharrisonlab)
- [Writing](https://substack.com/@ariharrisonlab)

## Leadership decisions

A selection of product, infra, and positioning calls made shipping NovoMCP (full version at [ariharrisonlab.github.io/#leadership](https://ariharrisonlab.github.io/#leadership)).

- **Two MCP servers, not one**: governance separation between free-tier and paid-only tools
- **Scale-to-zero by default**: every compute service ships with `min_replicas=0`
- **"Engine" never "platform"**: locked public language to one positioning noun
- **Killed the autonomous-campaign system**: replaced with human-in-the-loop via MCP elicitation
- **Free research-preview tier**: manually reviewed, auto-firing tier bump on signup
- **Private-endpoint-only infra**: build on GH-hosted runners, deploy via OIDC → SSM → bastion

---

*The system that makes the agent safe to deploy is the product.*
