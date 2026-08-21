<div align="left">

# Anubhav Joshi 

```text
┌────────────────────────────────────────────────────────────────────────┐
│  Backend Engineer (AI & Infrastructure) · 2026 CS Graduate             │
│  Open to Backend, AI Infrastructure, and Systems Engineering roles.    │
└────────────────────────────────────────────────────────────────────────┘
```
<div>
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=anubhav-qt&theme=github_dark" alt="GitHub Profile Details" height="160" />
</div>

---

### Tech Stack

<table>
  <tr>
    <td width="22%"><strong>Languages</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Python_3.11+-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
      <img src="https://img.shields.io/badge/SQL_(PostgreSQL_/_ClickHouse)-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL" />
    </td>
  </tr>
  <tr>
    <td width="22%"><strong>AI & Frameworks</strong></td>
    <td>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
      <img src="https://img.shields.io/badge/Google_Agent_Builder-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCP Agent Builder" />
      <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
      <img src="https://img.shields.io/badge/Model_Context_Protocol_(MCP)-FFCC01?style=flat-square&logo=clickhouse&logoColor=black" alt="MCP" />
    </td>
  </tr>
  <tr>
    <td width="22%"><strong>Data & Persistence</strong></td>
    <td>
      <img src="https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black" alt="ClickHouse" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="Postgres" />
      <img src="https://img.shields.io/badge/Neon_Serverless-00E599?style=flat-square&logo=neon&logoColor=black" alt="Neon" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
      <img src="https://img.shields.io/badge/pgvector_/_Pinecone-000000?style=flat-square&logo=pinecone&logoColor=white" alt="Vector Stores" />
    </td>
  </tr>
  <tr>
    <td width="22%"><strong>Cloud & DevOps</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCP" />
      <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
      <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel" />
      <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=black" alt="Render" />
    </td>
  </tr>
  <tr>
    <td width="22%"><strong>Web & Mobile UI</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" />
      <img src="https://img.shields.io/badge/React_Flow-FF0072?style=flat-square&logo=react&logoColor=white" alt="React Flow" />
      <img src="https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React Native" />
      <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white" alt="Expo" />
    </td>
  </tr>
</table>

---

### Building

<details>
<summary><strong>Continuum</strong>: AI-Native Virtual Film Studio OS & Production Continuity Coordinator</summary>
<br>

Built for Google Cloud's *Agentic Cinema Blockbuster Hackathon*. Most "AI movie" demos are single prompt chains: script in, video out, zero context remembered. **Continuum** coordinates the entire multi-million-dollar production lifecycle by modeling the movie as a persistent, queryable **Cyclic Production State Graph** backed by **ClickHouse** event sourcing and **Google Cloud Agent Builder**.

- **The core mechanic is invalidation, not blind regeneration.** If a director moves Scene 4 from a sunny park to a night warehouse, the engine calculates the upstream and downstream blast radius across schedule, call sheets, props, lighting rigs, and budget deltas, re-running only the affected agents.
- **Fixed-point convergence tames cyclic feedback loops.** To handle non-linear shooting and cyclic constraints without infinite recursion, the cascade runs in bounded 1-hop relaxation epochs with $O(1)$ differential payload hashing (`content_hash`) and an oscillation detector.
- **Collaborative negotiation over unprompted hallucination.** When a cascade breaches budget or schedule limits, the Negotiation Agent mediates a live multi-stakeholder chat with the Producer and Director, synthesizing constraint-respecting compromises (e.g. Day-for-Night VFX vs. Interior Soundstage).
- **Role-sliced projections with zero noise.** Crew members (Actors, Costume, Gaffers, Line Producers) only query materialized, craft-specific work orders. An actor sees their line cues and wound continuity; the costume lead sees wardrobe duplicates.
- **QC evaluates output against ground truth, not vibes.** Technical checks (framerate, black frames, audio balance) are pure deterministic code. Narrative and prop continuity checks trace directly to specific graph node IDs with provable diffs.
- **Stack:** Python 3.11+, Google Cloud Agent Builder (ADK), Gemini Enterprise, ClickHouse Cloud (`mcp-clickhouse`), FastAPI, React / Next.js with `@xyflow/react`.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/spoin_bundle">Spoin</a></strong>: Gamified Knowledge Feed Decoupled from Live LLM Latency</summary>
<br>

Spoin turns any topic into an algorithmic feed of bite-sized knowledge cards you scroll through like a social app, except progress is quiz-gated: you cannot unlock harder topics until proving mastery on earlier cards.

- **The user read path never calls an LLM.** A scroll requires sub-50ms latency, whereas generation takes seconds. The read and write paths are strictly decoupled via CQRS: background workers batch-generate and validate cards ahead of time into a Neon Postgres warehouse; the mobile/web feed reads only from indexed pre-computed stores.
- **Shared pool generation with ranking-based personalization.** Cards are generated once and shared globally rather than synthesized just-in-time per user. Personalization is computed as vector ranking and filtering over the shared corpus, slashing token costs by orders of magnitude while ensuring quality control happens once per card.
- **Fenced content guarantees.** Humor and ASCII scenes are strictly isolated into dedicated schema fields away from the factual explanation text, preventing creative tone from corrupting quiz assertions.
- **Stack:** FastAPI + SQLAlchemy (async), Neon Serverless Postgres with `pgvector`, local embedding models, Gemini Flash behind a swappable adapter interface, Next.js / React Native.
- Co-founded as a two-person team; authored system planning and 25 Architectural Decision Records (ADRs).

</details>

---

### Past Projects

<details>
<summary><strong><a href="https://github.com/anubhav-qt/trotter">Trotter</a></strong>: Deterministic Financial Valuation & Sentiment Engine</summary>
<br>

A trading research assistant scoring equities across weekly, monthly, and long-term horizons with live sentiment, technical momentum, and valuation grounding.

- **Deterministic scoring wall:** Momentum, volatility, volume profiles, and FinBERT sentiment are pure mathematical code over historical market data. Two identical queries return byte-identical scores; Gemini is only handed computed numbers for narrative synthesis.
- **Resilient aggregation with graceful degradation:** RSS feeds from Yahoo Finance and Google News are normalized against publisher title drift. If an external API key is missing, downstream steps gracefully skip while keeping core quantitative scorecards 100% operational.
- **Stack:** Next.js App Router, Server-Sent Events (SSE) progress streaming, FinBERT batched inference, 10-min symbol caching, Gemini Vision for candlestick chart analysis.

</details>

<details>
<summary><strong><a href="https://paribelle.in/">Paribelle</a></strong>: Production Storefront Engineered on a Multi-Vendor Schema</summary>
<br>

A live e-commerce platform selling designer apparel and jewellery, architected so an initial single-tenant deployment seamlessly scales to a multi-vendor marketplace without database migrations.

- **Schema-first multi-tenancy:** Products, orders, and settlements are isolated by vendor IDs at the schema level. Transitioning to a multi-merchant platform requires zero data re-architecture.
- **Dual-purpose control plane:** A unified admin interface serves both single-store inventory operations and platform-level marketplace administration.
- **Stack:** NestJS REST API, Next.js storefront & admin, Dockerized one-command seeded environment.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/fraud-vote-detection">Fraud Vote Detection</a></strong>: Computer Vision Audit Pipeline for Scanned Electoral Rolls</summary>
<br>

Automated audit pipeline converting scanned, printed voter grid images into structured, verifiable database records to detect fraudulent duplications.

- **OpenCV grid segmentation:** Segment and extract individual voter cells from noisy scanned document images.
- **GCP Vision OCR & Face Embedding Matching:** Reads text metadata with 98%+ crop accuracy and compares deep facial embeddings across the entire voter roll to catch individuals registered under multiple identities.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/synthetic-dataset-generator">Synthetic Dataset Generator</a></strong>: DCGAN for Privacy-Preserving Medical Imaging</summary>
<br>

Trained a Deep Convolutional GAN on the NIH chest X-ray dataset to synthesize high-fidelity 256×256 medical scans for data augmentation without patient privacy violations.

- **Mode-collapse prevention:** Implemented one-sided label smoothing, discriminator input noise injection, and asymmetric generator learning rates.
- **Performance:** Trained 125 epochs on RTX 3090, achieving an FID score of ~150 and generating 10,000+ validated synthetic scans.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/amazon-ml-challenge">Amazon ML Challenge</a></strong>: Multimodal Product Pricing Predictor</summary>
<br>

Built for Amazon's ML Challenge to predict price across 75,000 products from raw images, text metadata, and noisy titles.

- **Cold-brand calibration:** Handled a 60% unseen-brand test set distribution shift by dropping unreliable high-variance features and applying quantile mapping blended with raw model predictions.
- **Ensemble architecture:** 40 multimodal features fed into an Optuna-tuned ensemble of XGBoost, LightGBM, and neural networks, achieving 22.5% validation SMAPE.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/secondary-screen">Secondary Screen</a></strong>: Zero-Dependency Dashboard for Secondary Displays</summary>
<br>

A lightweight, zero-dependency auxiliary monitor dashboard replacing bloated 300MB Electron apps with clean web standards and an idempotent Windows launcher.

- **Architecture:** 3 static vanilla web files, a 40-line Python server, and an idempotent launcher that ensures single-instance execution on boot/wake without registry modifications.

</details>
<hr>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/anubhav-qt)
