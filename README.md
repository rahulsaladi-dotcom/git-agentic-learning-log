# tinker

> Think it. Tinker with it.

A personal productivity app — voice-first, distraction-free.

---

## Project structure

```
tinker/
├── app/
│   ├── layout.tsx        ← Root layout (fonts, metadata, wraps all pages)
│   ├── page.tsx          ← Landing page (route: /)
│   └── globals.css       ← Design tokens & base styles
├── components/
│   ├── Nav.tsx           ← Top navigation bar
│   └── VoiceButton.tsx   ← Voice recording button with state
├── styles/
│   └── landing.css       ← Landing page & component styles (add to globals.css)
├── tailwind.config.ts    ← Tailwind design tokens
└── README.md
```

---

## Getting started

### 1. Create the Next.js project (run this in your terminal, inside your repo folder)

```bash
npx create-next-app@latest . \
  --typescript \
  --tailwind \
  --eslint \
  --app \
  --src-dir=false \
  --import-alias="@/*"
```

When prompted:
- Would you like to use TypeScript? → **Yes**
- Would you like to use Tailwind CSS? → **Yes**
- Would you like to use the App Router? → **Yes**
- What import alias would you like? → **@/***

### 2. Copy the files

Replace the generated files with the ones from this project:
- `app/layout.tsx` → replace
- `app/page.tsx` → replace
- `app/globals.css` → replace with the base styles, then append `styles/landing.css` at the bottom
- `components/Nav.tsx` → create
- `components/VoiceButton.tsx` → create
- `tailwind.config.ts` → replace

### 3. Start the dev server

```bash
npm run dev
```

Open http://localhost:3000 — you should see the landing page.

---

## Key concepts in this codebase

| Concept | File | What it does |
|---|---|---|
| Root layout | `app/layout.tsx` | Wraps every page; loads fonts and metadata |
| CSS variables | `app/globals.css` | Design tokens — change here, updates everywhere |
| Server Component | `app/page.tsx` | Renders on server; fast, SEO-friendly |
| Client Component | `components/VoiceButton.tsx` | Runs in browser; handles clicks and state |
| `useState` | `VoiceButton.tsx` | Stores recording on/off state |
| `useEffect` | `VoiceButton.tsx` | Runs timer and keyboard listener as side effects |

---

## Tech stack

| Layer | Tool | Why |
|---|---|---|
| Framework | Next.js 14 (App Router) | Full-stack React — handles routing, server, and API |
| Language | TypeScript | Type-safe JavaScript — catches bugs before runtime |
| Styling | Tailwind CSS + custom CSS | Utility classes + design tokens |
| Fonts | next/font (Google Fonts) | Zero layout shift, self-hosted |
| Auth (soon) | Clerk | Drop-in authentication |
| Database (soon) | PostgreSQL via Prisma + Supabase | Relational DB, like Salesforce objects |
| Mobile (later) | Expo + React Native | Same logic, native iOS/Android UI |
