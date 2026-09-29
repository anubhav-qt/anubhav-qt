<div align="left">

# Anubhav Joshi

```
┌──────────────────────────────────────────────────────────────────────┐
│  Software Engineer · Builder                                         │
│  I like turning ambitious ideas into things that actually run.       │
└──────────────────────────────────────────────────────────────────────┘
```

I build and maintain products end to end — from the data model and backend to the interface, infrastructure, and the weird little details that make the product feel finished.

Most of my current work lives in four projects:

---

## Currently Building

<details open>
<summary><strong><a href="https://github.com/anubhav-qt/spoin_bundle">Spoin</a></strong> · Knowledge feed built around mastery</summary>
<br>

Spoin turns a topic into a structured learning journey: a fast swipeable feed of bite-sized knowledge, quizzes, deeper dives, and a curriculum designed to move from curiosity toward mastery.

- **The knowledge is curated first.** Spoin maintains a source-of-truth knowledge universe instead of treating an LLM's latent knowledge as the authority.
- **Generation is off the read path.** Cards are generated, verified, and stored asynchronously; the feed only serves completed content, keeping reads fast instead of waiting on inference.
- **Cards are shared, not regenerated per user.** Personalization happens through retrieval and ranking over the shared corpus, which keeps generation cost and quality control sane.
- **Learning is structured.** Curricula encode prerequisites and progression rather than throwing disconnected facts at the reader.
- **The system is deliberately multimodal.** Real visual anchors, diagrams, ASCII scenes, quizzes, and prose all have defined roles in the curriculum.
- Currently: **19 live topics, 12K+ cards, 7K+ quiz questions**, with the content-generation and serving systems being continuously expanded.

**Stack:** FastAPI · PostgreSQL · pgvector · SQLAlchemy · LangGraph · Gemini · Next.js · TypeScript

</details>

<details open>
<summary><strong><a href="https://github.com/anubhav-qt/breader">Breader</a></strong> · A minimal reader for the web</summary>
<br>

Breader is a reading environment built around one idea: the interface should disappear and let the book become the interface.

- **Books provide the colour.** Each title starts as an outline and fills in as you read, turning the library itself into a visual progress map.
- **Reads local-first.** EPUB, PDF, TXT, Markdown, and pasted text are supported without requiring an account.
- **Your position is exact.** Reading progress is saved to the character rather than the page, so it survives changes in window size and typography.
- **Built-in listening.** Browser-native voices, sentence highlighting, pronunciation overrides, immersive mode, and support for custom Piper/Kokoro voices.
- **Simple by design.** No ads, no subscriptions, no noisy dashboard — just a place to read.
- Open source under the **MIT License** and live at **[breader.site](https://breader.site)**.

**Stack:** React · TypeScript · Vite · browser storage · local TTS · open web APIs

</details>

<details open>
<summary><strong><a href="https://github.com/anubhav-qt/paribelle-ecosystem">PariBelle Ecosystem</a></strong> · Production commerce infrastructure</summary>
<br>

PariBelle is a live commerce ecosystem for fashion retail and marketplace operations, spanning the storefront, backend, administration, and warehouse/order management.

- **Full-stack commerce.** Catalogue, variants, cart, checkout, payments, orders, returns, wallet, invoices, GST/HSN, KYC, reviews, notifications, and administration.
- **Dedicated OMS.** <a href="https://github.com/anubhav-qt/pom">POM</a> handles inventory, reservations, picking, packing, dispatch, returns/RTOs, and marketplace operations.
- **Built to grow into multi-vendor.** Vendor-aware data modelling keeps the core system ready for marketplace expansion without rebuilding the schema.
- **Production engineering matters.** Idempotent payments, webhook verification, transactional inventory updates, authorization boundaries, rate limiting, realtime events, migrations, and automated QA are part of the system.
- **Actually in use.** PariBelle has been running in production since July 2026, with ongoing ownership of its codebase, infrastructure, fixes, and new features.

**Stack:** Next.js · React · NestJS · PostgreSQL · TypeORM · Docker · Razorpay · Cloudinary · Socket.IO

</details>

<details open>
<summary><strong><a href="https://github.com/anubhav-qt/my_website">my_website</a></strong> · My little corner of the internet</summary>
<br>

My personal site and dev log — part portfolio, part notebook, part place to document whatever I'm currently building.

- Projects are treated as actual things rather than résumé bullet points.
- Includes a scratchpad/dev-log, project writeups, contact page, and live project metrics.
- Designed and rebuilt repeatedly as my taste and ideas change.
- Live at **[anubhav-qt.dev](https://www.anubhav-qt.dev)**.

**Stack:** React 19 · TypeScript · Vite · Tailwind CSS · Supabase · Vercel

</details>

---

## Toolbox

<table>
  <tr>
    <td width="22%"><strong>Languages</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
      <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" alt="C++" />
      <img src="https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white" alt="SQL" />
    </td>
  </tr>
  <tr>
    <td><strong>Backend & Data</strong></td>
    <td>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
      <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" alt="NestJS" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
      <img src="https://img.shields.io/badge/pgvector-000000?style=flat-square&logo=postgresql&logoColor=white" alt="pgvector" />
    </td>
  </tr>
  <tr>
    <td><strong>AI & Systems</strong></td>
    <td>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
      <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square" alt="LangGraph" />
      <img src="https://img.shields.io/badge/Computer_Vision-5C3EE8?style=flat-square" alt="Computer Vision" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
      <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
    </td>
  </tr>
  <tr>
    <td><strong>Frontend</strong></td>
    <td>
      <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" />
      <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" />
      <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
    </td>
  </tr>
</table>

---

<div align="center">

[![Website](https://img.shields.io/badge/anubhav--qt.dev-111111?style=flat-square&logo=vercel&logoColor=white)](https://www.anubhav-qt.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/anubhav-qt)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/anubhav-qt)

<sub>Build things. Keep them alive. Make them weird.</sub>

</div>
