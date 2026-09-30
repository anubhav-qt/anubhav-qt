<div align="left">

# Anubhav Joshi 

```text
┌────────────────────────────────────────────────────────────────────────┐
│  Backend Engineer · 2026 CS Graduate                                   │
│  Generative AI Engineer Trainee @Precision Design & Engineering        │
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
<summary><strong><a href="https://github.com/anubhav-qt/spoin_bundle">Spoin</a></strong>: For the Curious</summary>
<br>

Spoin started as a simple idea: make a learning app that feels like scrolling a social feed. Pick some topics, get one thing to learn, then another, with quizzes and progression so it does not turn into an endless pile of random facts.

The first version was basically Gemini generating cards from "trust me bro". That worked for a while. Then the corpus got large enough that I had to rebuild the knowledge side properly.

Now `the_spoin_universe` is the source of truth. FROG retrieves from it before generation, verification gets its own evidence, cards are generated ahead of time, and the feed never has to wait for an LLM call.

The other half of Spoin is the learning system around the cards. Curricula describe what should be taught and in what order. Deterministic checks validate the generated structure. Users can report broken cards, bad diagrams, broken art and other issues, which I review in the admin panel and fix manually.

The models are workers now. They are not Spoin.

**Stack:** FastAPI · PostgreSQL · pgvector · FROG · LangGraph · Gemini · Next.js · React

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/breader">Breader</a></strong>: A Minimal Reader for the Web</summary>
<br>

I wanted a place where I could open a book and just read without the site trying to turn reading into a productivity dashboard.

So Breader is deliberately quiet. Books start as outlines in the library and fill with their own colour as you read, until a finished book is completely filled. Your position is saved to the character, the reader has both paged and scroll modes, and the controls stay out of the way.

Then I kept adding the things I actually wanted while reading. Browser-side voices. Sentence highlighting. Pronunciation overrides. Immersive mode. Custom Piper and Kokoro voices.

EPUB, PDF, TXT, Markdown and pasted text all work. There is no account requirement, no ads and no subscription.

**Stack:** React · TypeScript · Vite · browser storage · local TTS

</details>

<details>
<summary><strong><a href="https://www.paribelle.in">PariBelle Ecosystem</a></strong>: Fashion Commerce from Storefront to OMS</summary>
<br>

PariBelle is the commerce system I have been building across the storefront, backend, admin and OMS.

The customer side handles the shopping flow. The backend handles the parts that become important once real orders start moving: variants, inventory, payments, GST/HSN, invoices, KYC, returns, wallet and notifications.

The system is split into separate pieces. The Next.js storefront and admin talk to a NestJS API, and POM handles the warehouse side with inventory ledgers, reservations, picking, packing, dispatch, returns and marketplace operations.

The data model is vendor-aware from the start because I do not want multi-vendor to become a future rewrite.

It has been running in production since July 2026. I have kept working on the same system after deployment, adding features, fixing things as they appear and changing parts of the architecture when the existing shape stops making sense.

**Stack:** Next.js · React · NestJS · PostgreSQL · TypeORM · Docker · Razorpay · Cloudinary · Socket.IO

</details>

<details>
<summary><strong><a href="https://github.com/anubhav-qt/my_website">my_website</a></strong>: My Little Corner</summary>
<br>

This is the website I keep rebuilding whenever I change my mind about how I want my work to look.

It started as a portfolio. It turned into a project archive, then a dev log, then the Scratchpad where I dump writeups, half-formed ideas, technical rabbit holes and whatever I was obsessing over that week.

The project pages have their own writeups and live metrics. The Scratchpad is where I write the longer versions of things after I have actually spent enough time building them to know what happened.

A lot of the Spoin documentation ended up there because writing "Gemini pissed me off, so I rebuilt the architecture" is a much better explanation of the project than pretending it arrived fully designed.

**Stack:** React 19 · TypeScript · Vite · Tailwind CSS · Supabase · Vercel

</details>

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/anubhav-qt)
