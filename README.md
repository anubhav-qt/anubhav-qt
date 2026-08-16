## Anubhav Joshi

Backend Engineer (AI / Infrastructure). CS graduate, Rajasthan, India.

The part of an AI system I find interesting is the part that isn't the model: persistent
state, dependency graphs, and knowing which work to keep away from an LLM entirely.

> **Models are trusted for taste, never for constraints.**
> Anything that must be *true* is enforced in code. Anything that merely needs to be
> *good* is the model's job.

Open to backend and AI infrastructure roles.

```
Languages   Python · TypeScript
AI/ML       PyTorch · LangChain · LangGraph
Backend     FastAPI · Postgres · pgvector · Redis · Docker
Infra       GCP · Neon · Render · Vercel
Web         Next.js
```

---

### Building now

### Building

* **[Spoin](https://github.com/anubhav-qt/slocho_bundle)**: Swipeable AI knowledge feed.
  * **Zero-LLM Read Path:** Kept LLM calls off the feed for ~50ms swipe latency; generation runs in batched background pipelines.
  * **Stack & Scale:** FastAPI, SQLAlchemy Async, Neon (Postgres + pgvector), Gemini Flash, Next.js. Architected across 25 ADRs.

* **Agentic Cinema**: AI-native virtual film studio engine.
  * **State Invalidation:** Treats production as a connected graph where updating one node invalidates only actual dependent sub-graphs (schedules, permits, shot designs).
  * **Human-in-the-Loop:** Event-sourced state layer with bounded agent loops and deterministic QC gates.

### Secondary Projects

* **paribelle ([backend](https://github.com/anubhav-qt/paribelle-backend)** + **[web](https://github.com/anubhav-qt/paribelle-web))**: Single-store commerce platform (NestJS API and Next.js storefront/admin, Dockerized with one-command seeded setup).
* **[fraud-vote-detection](https://github.com/anubhav-qt/fraud-vote-detection)**: Automated electoral roll fraud scanner using OpenCV grid segmentation, Google Cloud Vision OCR (98%+ accuracy), and deep learning face encodings.
* **[synthetic-dataset-generator](https://github.com/anubhav-qt/synthetic-dataset-generator)**: DCGAN for synthetic chest X-rays (FID ~150 over 125 epochs).
* **[amazon-ml-challenge](https://github.com/anubhav-qt/amazon-ml-challenge)**: Multimodal price prediction over 75k products using LightGBM/XGBoost ensembles.
* **[secondary-screen](https://github.com/anubhav-qt/secondary-screen)**: Zero-dependency 40-line portrait monitor dashboard.

---

### How I Work

* **Own the system, not a layer.** Schema and state design, API, workers, deploy, and the developer experience that lets someone else clone it and ship the same day.
* **Build pipelines around models rather than on top of them.** Training GANs, ensembling over vision and text features, batching LLM generation behind a swappable interface, and using vision models to verify rather than to author.
* **Deterministic where determinism is cheaper.** Budgets, diffs, and format checks are code, not model calls. Anything that can re-trigger itself gets an iteration cap and a human gate.
* **State is the source of truth; models interpret it.** A fact you can assert against beats a fact the model has to remember.
* **Plan first, then enforce it.** Real decisions become documents, not comments. Docs rot silently; a failing CI check does not.
* **Cost is a design constraint, not a retrofit.** Free tier first, local where local is free, reasoning effort matched to the stage that needs it.
---

[LinkedIn](https://linkedin.com/in/anubhav-qt)
