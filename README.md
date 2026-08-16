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

**[Spoin](https://github.com/anubhav-qt/slocho_bundle)** is a swipeable feed of
AI-generated knowledge cards, quiz-gated so progression means something. One constraint
shapes it: **the feed read path never touches an LLM.** A swipe is ~50ms and a generation
call is seconds, so the system splits into a batched content factory, a Postgres and
pgvector warehouse, and a serving layer that is fast because it does no inference. Cards
are generated once and shared, so personalization is ranking, not per-user generation.
FastAPI, SQLAlchemy async, Neon, Gemini Flash, Next.js. Two-person team; I own
architecture, planning, and design, across 25 ADRs.
*(The repo is still `slocho_bundle`: the rename to Spoin is committed to one atomic sweep
rather than done piecemeal, so the tree stays answerable in the meantime.)*

**Agentic Cinema** is an AI-native virtual film studio. A film is a connected production
graph, not a pile of documents, so editing one node marks its *actual* dependents stale
(schedule, permits, props, shot design, budget) and the responsible agents re-derive only
what changed, under convergence checks with a human gate when they don't agree. The hard
problem isn't generation. It's invalidation.
Gemini and Agent Builder over an event-sourced state layer, with deterministic QC.
*In build; repo goes public at submission.*

### Also

- **[synthetic-dataset-generator](https://github.com/anubhav-qt/synthetic-dataset-generator)**
  DCGAN for synthetic chest X-rays, addressing medical data scarcity. Most of the work was
  training stability: label smoothing, noise injection, asymmetric learning rates. FID ~150
  over 125 epochs.
- **[amazon-ml-challenge](https://github.com/anubhav-qt/amazon-ml-challenge)**
  Multimodal price prediction over 75k products, 22.5% SMAPE. Image and text features into
  an XGBoost/LightGBM/NN ensemble, with calibration for a train/test brand distribution
  shift that made 60% of test brands unseen.
- **[secondary-screen](https://github.com/anubhav-qt/secondary-screen)**
  A portrait-monitor dashboard. Three static files, a 40-line server, no build step and no
  dependencies. Running the launcher twice gives you one window, not two.

---

### How I work

- **Own the system, not a layer.** Schema and state design, API, workers, deploy, and the
  developer experience that lets someone else clone it and ship the same day. I build the
  clients too, but the thinking happens behind the API.
- **Build pipelines around models rather than on top of them.** Training GANs, ensembling
  over vision and text features, batching LLM generation behind a swappable interface, and
  using vision models to verify rather than to author.
- **Deterministic where determinism is cheaper.** Budgets, diffs, and format checks are code,
  not model calls. Anything that can re-trigger itself gets an iteration cap and a human gate.
- **State is the source of truth; models interpret it.** A fact you can assert against beats
  a fact the model has to remember.
- **Plan first, then enforce it.** Real decisions become documents, not comments. Docs rot
  silently, a failing CI check does not.
- **Cost is a design constraint, not a retrofit.** Free tier first, local where local is free,
  reasoning effort matched to the stage that needs it.

---

[LinkedIn](https://linkedin.com/in/anubhav-qt)
