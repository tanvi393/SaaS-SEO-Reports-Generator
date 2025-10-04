# 🚀 SaaS SEO Reports Generator

A **comprehensive SEO analysis platform** that generates beautiful, AI-powered, data-driven reports. Built with **Next.js 15**, **Clerk authentication**, **Convex backend**, and powered by **Bright Data’s Perplexity Scraper** with **OpenAI GPT analysis**.

---

## 🌟 Features

### 🔹 For Users

* ⚡ **Instant SEO Reports** – Generate SEO analysis in seconds using AI.
* 🧩 **Entity Analysis** – Analyze businesses, people, products, courses, or websites.
* 💬 **AI Chat Integration** – Chat with your reports using **OpenAI GPT-4o** (model customizable in code).
* 📊 **Comprehensive Data** – Inventory sourcing, competitor analysis, keyword research, backlink analysis.
* ⏱ **Real-time Progress** – Live status updates while reports are generated.
* 🎨 **Beautiful Dashboard** – Modern, responsive UI with detailed visualizations.

### 🔹 Technical Features

* **Next.js 15 (App Router)** with **React 19** and **Turbopack**
* **Clerk Authentication** + Billing (Stripe) with Starter/Pro plans
* **Convex Backend** for serverless functions, real-time data, and job management
* **Bright Data SERP & Perplexity Scraper** for deep SEO data collection
* **OpenAI GPT-4o** for structured analysis & report generation
* **TypeScript + Zod Validation** for strict type safety
* **shadcn/ui + Radix UI + Tailwind v4** for modern, accessible components

---

## 🧠 AI & Data Processing

* **Smart Web Scraping** – Bright Data + Perplexity integration.
* **Structured AI Analysis** – Validated with Zod schemas.
* **Background Processing** – Convex schedulers for long-running tasks.
* **Smart Retry Logic** – Re-run failed analyses without re-scraping.
* **Evidence-Based Reports** – Insights with source attribution and quotes.

---

## 📂 Project Structure

```
app/                  → Next.js App Router pages & layouts
  page.tsx            → Marketing homepage (features & pricing)
  dashboard/          → Protected dashboard for report management
  report/[id]/        → Individual report pages
  summary/            → Detailed SEO report analysis
  ui/                 → Visualization components

api/chat/             → AI chat API endpoint
components/           → Reusable UI, providers, chat interface
convex/               → Backend functions & database schema
  schema.ts           → Convex DB schema
  scrapingJobs.ts     → Job management
  analysis.ts         → AI workflows
  http.ts             → Webhook handlers (Bright Data)

actions/              → Server actions (e.g., scraping, retries)
prompts/              → AI prompt engineering (Bright Data, OpenAI)
lib/                  → Utilities, helpers, validation schemas

middleware.ts         → Auth protection for /dashboard routes
auth.config.ts        → Clerk authentication configuration
```

---

## 🔄 Data Flow

1. **User Input** – Entity + country selected in dashboard.
2. **Job Creation** – `startScraping.ts` creates a job record in Convex.
3. **Web Scraping** – Bright Data’s Perplexity Scraper collects raw data.
4. **Webhook Processing** – Data sent to `/api/webhook`.
5. **AI Analysis** – OpenAI GPT-4o processes data via structured prompts.
6. **Report Generation** – SEO report stored, validated, and visualized.
7. **AI Chat** – Pro users chat with reports using contextual AI.

---

## 🔐 Authentication & Authorization

* **Clerk Auth** – Protects `/dashboard` routes via `middleware.ts`.
* **Clerk + Stripe Billing** – Subscription tiers (Starter / Pro).
* **Feature Gating** – Pro plan required for AI chat & advanced analysis.

---

## ⚙️ Background Processing

* **Convex Schedulers** – Handle async analysis jobs.
* **Smart Retry** – Retry failed analyses without re-scraping.
* **Real-Time Updates** – Dashboard updates as jobs progress.

---

## 🤖 AI Features

* ✅ **Structured Analysis** – Consistent schema via Zod.
* 🔎 **Evidence-Based** – Reports include source links & quotes.
* 🧠 **Contextual AI Chat** – Conversational assistant with full report context.
* 🌍 **Web Search Integration** – Chatbot can extend with live searches.

---
## 📊 Example Use Cases

* Generate **SEO reports** for competitors
* Perform **keyword + backlink analysis**
* Track **feature adoption** across websites
* Provide **executive dashboards** for SaaS clients

---

## 🛠️ Tech Stack

* **Frontend**: Next.js 15, React 19, shadcn/ui, TailwindCSS
* **Backend**: Convex, Clerk, Stripe
* **AI/ML**: OpenAI GPT-4o, Bright Data Perplexity Scraper
* **Validation**: TypeScript + Zod
* **Visualization**: Custom UI + Tailwind
