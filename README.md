## Anubhav Joshi

Backend Engineer (AI / Infrastructure). 2026 CS graduate, Rajasthan, India.

The part of an AI system I find interesting is the part that isn't the model: persistent
state, dependency graphs, and knowing which work to keep away from an LLM entirely.

> **Models are trusted for taste, never for constraints.**
> Anything that must be *true* is enforced in code. Anything that merely needs to be
> *good* is the model's job.

*Open to backend and AI infrastructure roles.*

<hr>

### Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Postgres](https://img.shields.io/badge/Postgres-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?style=flat-square)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)

[![GitHub Stats](https://github-stats-extended.vercel.app/api?username=anubhav-qt&rank_icon=github&hide_title=true&show_icons=true&theme=dark)](https://github-stats-extended.vercel.app/api?username=anubhav-qt&rank_icon=github&hide_title=true&show_icons=true&theme=dark)

---
### Building

<details>
<summary><strong><a href="https://github.com/anubhav-qt/spoin_bundle">Spoin</a></strong>: Scroll-and-learn knowledge feed, gamified with quizzes instead of just autoplay</summary>
<br>

Spoin turns any topic into a feed of short AI-written knowledge cards you scroll through
like a social app, except progress is quiz-gated: you don't move to harder material until
you've actually shown you understood the easier card. It's built to solve a real problem
with existing "learn on your phone" apps, which are either static courses (no feed feel) or
pure entertainment feeds (no learning gate).

- **The feed never calls an LLM.** A scroll needs to feel instant (~50ms), and a generation
  call takes seconds, so the two are fully decoupled. A background pipeline writes cards
  into Postgres in batches ahead of time; the feed only ever reads from that warehouse. This
  is the single decision the rest of the architecture is built around.
- **Cards are generated once and shared across every user**, not regenerated per person.
  Personalization happens by re-ranking the same shared pool of cards, not by asking the
  model to write a new one for you. Much cheaper, and it means quality control only has to
  happen once per card, not once per view.
- **Humor is fenced off from the part you're tested on.** A card can be playful in its title
  or a small ASCII scene, but the actual explanation is kept in a separate, straight-prose
  field. That's what keeps a joke from corrupting a fact you're being quizzed on.
- **Stack:** FastAPI + SQLAlchemy (async) on Neon Postgres with pgvector, local embeddings,
  Gemini Flash behind a swappable interface so the model can change without touching the
  rest of the app, Next.js on the frontend.
- Two-person team. I own the architecture, planning and system design; 25 ADRs written so
  far, each one a real decision with the reasoning kept alongside it.

</details>

<details>
<summary><strong>Continuum</strong>: An AI production studio that runs a movie from screenplay to final cut as one continuous, stateful project</summary>
<br>

Built for a Google Cloud agentic hackathon. Most "AI makes a movie" demos are a single
prompt chain: script in, video out, nothing remembered in between. This is built the
opposite way: the whole production (story, characters, locations, schedule, budget, shots)
is stored as one connected graph of state that every stage reads from and writes to, so a
change made on day one is still correctly reflected in the final cut.

- **The core mechanic is invalidation, not generation.** If a producer moves a scene from a
  police station to an airport, that one edit has to correctly mark the schedule, permits,
  props, shot design, budget and call sheet as stale, and only those, then re-run exactly
  the agents responsible for each, and converge without looping forever. That cascade, not
  the video output, is the actual hard problem this project solves.
- **State and reasoning are kept separate on purpose.** Facts about the production live in a
  deterministic, queryable store. A Continuity Agent reads that store and reasons over it,
  instead of being asked to remember the whole movie in its own head, which is where these
  systems normally start hallucinating.
- **Loops are bounded on purpose.** A hard cap on re-run iterations, a convergence check
  that stops the cascade once nothing new goes stale, and a human approval gate before any
  change is allowed to rewrite the original brief.
- **QC checks the movie against the plan, not against vibes.** Technical checks (resolution,
  frame rate, sync) are plain code. Story and continuity checks trace back to a specific
  node in the state graph, so every flagged issue is provable, not just a model's opinion.
- Gemini + Agent Builder for orchestration, over an event-sourced state layer, with
  deterministic checks doing the parts that don't need a model at all.

</details>

### Past Projects

<details>
<summary><strong><a href="https://github.com/anubhav-qt/trotter">Trotter</a></strong>: Technical Analysis and Research of Stock Market with AI</summary>
<br>

A trading assistant that scores any stock across three time horizons (weekly, monthly,
long-term) and backs it with live sentiment, technicals, and web-grounded valuation. The
project's one hard rule is the same one that governs how I use models anywhere: anything
that has to be *true* — a momentum figure, a P/E band, a volatility read — is computed in
code from real market data, and Gemini is only ever handed the finished numbers to explain.

- **The scoring engine never touches an LLM.** Momentum, valuation, volume, sentiment and
  volatility are all deterministic functions over price history, quote data, and FinBERT
  output. Two identical searches now return byte-identical scores; only the model's prose
  and target-price estimate are allowed to vary run to run.
- **News is aggregated across two independent RSS sources** (Yahoo Finance and Google News)
  and deduplicated against title drift — Google News appends `" - Publisher"` to every
  headline, which silently broke naive dedup before it was normalized out.
- **FinBERT sentiment is batched**, not called per-headline, so a 30-day news window
  classifies as one pipeline pass instead of N sequential model invocations.
- **Every external dependency degrades instead of failing.** No `GOOGLE_API_KEY`? You still
  get full quantitative scores, just without narrative commentary. No `TAVILY_API_KEY`? The
  industry P/E step is skipped, nothing else breaks.
- Next.js App Router with an SSE endpoint streaming pipeline progress live to the client,
  a 10-minute per-symbol cache so repeat lookups are instant, and a Gemini vision "Deep
  Dive" mode that reads the rendered candlestick chart and can nudge scores within a capped
  delta — visual read, not a fresh number from scratch.

</details>

<details>
<summary><strong><a href="https://paribelle.in/">paribelle</a></strong>: A real single-vendor storefront, built on a multi-vendor schema</summary>
<br>

A working commerce site selling designer kurtis and artificial jewellery. The backend
still models every product as belonging to a vendor, on purpose: there's only one vendor
seeded in right now, but the schema, the admin panel and the API are all built as if there
could be more, so the marketplace version isn't a rewrite later, just a data change.

- NestJS API ([backend repo](https://github.com/anubhav-qt/paribelle-backend)) and Next.js
  storefront + admin panel ([web repo](https://github.com/anubhav-qt/paribelle-web)).
- One admin panel does double duty as both the store owner's dashboard and what would be
  the platform-level admin in a multi-vendor version.
- Fully Dockerized with a one-command seeded setup: schema, categories and sample products
  are all created by a single init command, so a fresh clone has a working store in minutes.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/fraud-vote-detection">fraud-vote-detection</a></strong>: Scans scanned electoral rolls for duplicate or fraudulent voter entries</summary>
<br>

Indian electoral rolls are distributed as scanned images of printed grids, which makes them
easy to skim but hard to audit at scale. This pipeline turns a scanned roll into structured,
checkable data and flags entries that look duplicated or fabricated.

- **OpenCV grid segmentation** first isolates each individual voter cell from the scanned
  page, since the source is a printed table image, not structured text.
- **Google Cloud Vision OCR** then reads the name, age and address out of each cell, at
  98%+ accuracy on the segmented crops.
- **Deep learning face encodings** compare the photo in each entry against the rest of the
  roll, to catch the same person registered more than once under different details, which
  plain text matching alone would miss.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/synthetic-dataset-generator">synthetic-dataset-generator</a></strong>: A GAN that generates realistic synthetic chest X-rays</summary>
<br>

Medical imaging datasets are hard to get: they're small, and sharing real patient scans
raises privacy problems. This trains a DCGAN to generate realistic-looking chest X-rays
from the NIH dataset, so the synthetic output can be used to augment training data or
shared without touching real patient images.

- 7-layer generator (~1.8M parameters) turning random noise into 256×256 grayscale images,
  against a 7-layer discriminator (~2.4M parameters) trained to tell real from fake.
- The real engineering problem in a GAN is stopping it from collapsing to a handful of
  repeated outputs. That's handled here with label smoothing, noise injected into the
  discriminator's inputs, and a learning rate that deliberately favors the generator.
- Trained 125 epochs on an RTX 3090 (about 8 to 10 hours), reaching an FID of roughly 150,
  which is within the normal range for medical imaging GANs, and generating over 10,000
  usable synthetic images.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/amazon-ml-challenge">amazon-ml-challenge</a></strong>: Predicts product prices from a mix of product images and text</summary>
<br>

Built for Amazon's 2025 ML Challenge: predict price for 75,000 real products using
whatever combination of image, text and metadata is available, which is closer to a real
pricing problem than a clean single-input dataset.

- Extracted 40 features total: 18 from image quality signals, 22 from the product's text
  and title, then fed both into a three-model ensemble (XGBoost, LightGBM, and a small
  neural net tuned with Optuna), combined by weighted averaging.
- The harder problem was that the test set didn't match training: 60% of test-set brands
  had never been seen in training. Unreliable features were dropped and predictions were
  calibrated with quantile mapping blended against the raw model output, specifically to
  correct for that mismatch.
- Reached 22.5% SMAPE on validation, with the full 75,000-row inference run completing in
  under a minute.

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/secondary-screen">secondary-screen</a></strong>: A zero-dependency dashboard for a spare portrait monitor</summary>
<br>

A lot of second-monitor dashboards are Electron apps with a build step for what's really
just a clock, a to-do list and a video player. This is the opposite: three static files, a
40-line Python server, and a Windows launcher, nothing else.

- No framework and no build step. Plain HTML, CSS and JS that will run in any modern
  browser; only the launcher is Windows-specific.
- The launcher is idempotent on purpose: it checks what's already running before starting
  anything, so running it twice (or it firing again after sleep/wake) gives you one window
  in the right place, not a second stacked on top.
- Installs as one Startup-folder shortcut, no admin rights and no registry changes, so
  removing it is deleting a single `.lnk` file.

</details>
---
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/anubhav-qt)
