<div align="left">

# Anubhav Joshi 

```text
┌────────────────────────────────────────────────────────────────────────┐
│  Backend Engineer · 2026 CS Graduate                                   │
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
    </td>
  </tr>
  <tr>
  <td width="22%"><strong>AI & ML</strong></td>
  <td>
    <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
    <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
    <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain" />
    <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
    <img src="https://img.shields.io/badge/Computer_Vision-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="Computer Vision" />
  </td>
</tr>
  <tr>
    <td width="22%"><strong>Data & Persistence</strong></td>
    <td>
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
      <img src="https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React Native" />
      <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white" alt="Expo" />
    </td>
  </tr>
</table>

---

### Building

<details>
<summary><strong>Spoin</strong>: A Grounded, Mastery-Driven Knowledge Feed</summary>
<br>

Spoin turns any topic into a personalized feed of bite-sized knowledge cards designed to take a learner from curiosity to mastery.

- **Knowledge is separated from generation.** Spoin maintains a curated source-of-truth knowledge universe, `the_spoin_universe`, rather than relying on an LLM's latent knowledge as the content authority. Topics and curricula are constructed from this shared semantic substrate, allowing knowledge to be reused across domains instead of rebuilding isolated topic corpora.
- **FROG provides grounded retrieval.** The Spoin-specific RAG layer retrieves relevant evidence from `the_spoin_universe` before generation. Generators synthesize from retrieved evidence, while separate thinker/verifier models evaluate the result. The model proposes; deterministic validation enforces structural contracts.
- **Learning architecture is explicit.** Curricula are built around prerequisite relationships and a progression from hook → concept → mental model → mechanism → example → discrimination → misconception → application → integration → retrieval. Difficulty increases through reasoning, diagnosis, transfer, and multi-system trade-offs rather than simply adding jargon.
- **Pre-generated, asynchronous serving.** Generation and verification happen off the read path, allowing the learner's feed to serve completed cards without waiting on live LLM inference. Model providers are isolated behind replaceable generation/verification interfaces.
- **Multimodal grounding is deliberate.** Curated visual anchors, generated diagrams/ASCII, and deterministic layout validation are used according to their pedagogical role rather than as decoration. Visuals are grounded in the same knowledge architecture as the cards.
- **Stack:** FastAPI + SQLAlchemy (async), PostgreSQL, vector retrieval, FROG, pluggable LLM generators/verifiers, and a Next.js / React-based client.
- Co-founded as a two-person team; authored the system architecture, knowledge/corpus methodology, curriculum architecture, and architectural decision records.

</details>

<details>
<summary><strong><a href="https://www.paribelle.in">PariBelle</a></strong>: Production Commerce Ecosystem for Fashion Retail & Marketplace Operations</summary>
<br>

PariBelle is a live e-commerce ecosystem spanning the customer storefront, commerce backend, unified administration, and warehouse/order management, architected to support both a single-brand deployment and future multi-vendor marketplace operations.

- **End-to-end commerce platform.** The customer-facing system covers catalogue discovery, product variants, cart and checkout, payments, orders, returns/exchanges, wallet, invoices, GST/HSN, KYC, reviews, notifications, and marketplace-ready vendor management.
- **Unified control plane.** A single admin application manages products, orders, categories, homepage content, custom pages, policies, invoices, KYC, analytics, filters, store settings, and other operational workflows.
- **Dedicated OMS.** [POM](https://github.com/anubhav-qt/pom) handles warehouse and marketplace operations including order ingestion, SKU mapping, inventory ledgers, reservations, pick/pack/dispatch workflows, shipping labels, returns/RTOs, and marketplace integrations.
- **Schema-first multi-tenancy.** Products, orders, inventory, and settlements are isolated by vendor identifiers at the data-model level, allowing the platform to evolve from a single-brand deployment into a multi-vendor marketplace without re-architecting the core schema.
- **Production-oriented engineering.** Payment idempotency, webhook verification, transactional inventory updates, authorization boundaries, rate limiting, realtime notifications, automated checks, migrations, and documented production QA are built into the system rather than treated as post-launch additions.
- **Stack:** [NestJS REST API](https://github.com/anubhav-qt/paribelle-backend), [Next.js / React storefront & admin](https://github.com/anubhav-qt/paribelle-web), [POM OMS](https://github.com/anubhav-qt/pom), PostgreSQL, Dockerized development environment, Razorpay, Cloudinary, Socket.IO, and marketplace integrations.
- Built as a production system for PariBelle; responsible for the system architecture, implementation direction, testing, maintenance, and evolution across the storefront, backend, administration, and OMS.

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
