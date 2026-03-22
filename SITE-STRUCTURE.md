# Site Structure: URL Architecture

## Full URL Hierarchy

```
/
├── /                          ← Homepage: "Build + Automate with AI"
│
├── /build                     ← Pillar: Ship Products with AI
│   ├── /build/apps
│   ├── /build/mvp
│   └── /build/tools
│
├── /automate                  ← Pillar: Automate Your Work with AI
│   ├── /automate/workflows
│   ├── /automate/agents
│   └── /automate/systems
│
├── /method                    ← The 4-step system (Idea → Product → Automation)
│
├── /work                      ← Proof: Case studies split by Build / Automate
│   ├── /work/builds
│   └── /work/automations
│
├── /learn                     ← Course landing page
├── /sprint                    ← Sprint landing page (1:1 / done-with-you)
│
├── /blog                      ← Content engine
│   ├── /blog/build/           ← Build category
│   ├── /blog/automate/        ← Automate category
│   └── /blog/case-studies/    ← Social proof + SEO
│
├── /tools                     ← Free resource: AI tool stack / starter kit
│
├── /about
└── /start                     ← Primary CTA destination
```

---

## Key Architecture Decisions

- **`/build` and `/automate` as top-level pillars** signal topical authority to Google independently
- **`/method` is a standalone SEO page** for searches like "AI build system" or "idea to product framework" — also carries `HowTo` schema
- **`/tools` free resource** is a link magnet and captures tool-comparison traffic
- **`/blog` split into two categories** lets you build keyword authority in both clusters independently
- **`/work` split into builds vs automations** makes proof scannable and feeds both pillar keyword clusters
- **`/start` as the CTA destination** keeps conversion tracking clean (single goal URL)

---

## Internal Linking Strategy

Every blog post should:
1. Link back to its pillar page (`/build` or `/automate`)
2. Link to 1–2 related posts within the same category
3. Link to `/method` when referencing the system
4. Link to `/learn` or `/sprint` near the CTA

Pillar pages should:
1. Link to all blog posts in their category
2. Cross-link to each other (build ↔ automate — the combination is the product)
3. Link to `/work` case studies as proof

---

## Page Priorities (Launch Order)

| Priority | Page | Reason |
|---|---|---|
| 1 | `/` | First impression + keyword anchor |
| 2 | `/method` | Unique IP — own the "system" framing |
| 3 | `/work` | E-E-A-T foundation — proof before offer |
| 4 | `/learn` + `/sprint` | Conversion pages |
| 5 | `/build` + `/automate` | Pillar pages for topical authority |
| 6 | `/tools` | Link magnet |
| 7 | `/blog/*` | Content engine — ongoing |
