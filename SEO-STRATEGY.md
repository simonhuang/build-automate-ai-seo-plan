# SEO Strategy: AI Build + Automate Platform

## Business Classification

**Type:** Creator-educator / course seller
**Niche:** AI product building + workflow automation (no-code angle)
**Stage:** New site — no existing authority
**Primary monetization:** Course + Sprint (done-with-you)

---

## Competitive Landscape

| Competitor Type | Who they are | Their gap |
|---|---|---|
| Build-only creators | "Build apps with AI" YouTubers, Replit tutorials | Stop at the product — no automation |
| Automation-only tools | Zapier/Make.com content, n8n docs | Too tool-specific, no product building |
| No-code educators | Makerpad, Webflow University | Not AI-native, not automation-focused |
| Vibe coding wave | Twitter/X builders | No curriculum, no transformation arc |

**White space:** The "build *and* automate" combination is genuinely unclaimed as a distinct positioning. Nobody owns the keyword cluster that bridges "ship a product" + "automate the work around it."

---

## Keyword Strategy

### Tier 1 — Primary (own these first)

| Keyword | Intent | Why it fits |
|---|---|---|
| `build and automate with AI` | Navigational/commercial | Exact positioning phrase — low competition now |
| `AI workflow automation course` | Commercial | High intent, course buyer |
| `build apps with AI no code` | Informational → commercial | Entry point keyword |
| `automate repetitive tasks with AI` | Informational | Pain-aware searcher |
| `AI automation for non-developers` | Informational | Sharp targeting of your audience |

### Tier 2 — Content/blog traffic (build authority)

| Keyword cluster | Content type |
|---|---|
| `how to automate [X] with AI` | Tutorial series (high volume via long-tail) |
| `build an MVP with AI in [X days]` | Case study / guide |
| `AI agents for automation` | Explainer — topical authority |
| `replace [job task] with AI workflow` | Specific pain-point posts |
| `vibe coding + automation` | Trend-riding — combines two search waves |
| `best AI tools to build and automate` | Tool roundup (affiliate potential) |

### Tier 3 — GEO / AI search (get cited)

Phrases that should make AI Overviews cite you:
- "what is the fastest way to build with AI"
- "can you automate workflows without coding"
- "how to turn an idea into a product with AI"

---

## E-E-A-T Strategy

This is a YMYL-adjacent niche (people are making business decisions). Trust signals from day one:

1. **Experience signals:** Every blog post should reference a real build or automation you did. Screenshots, tool outputs, before/after metrics.
2. **Expertise signals:** Author bio with specific credentials — not "AI expert" but "built 20+ AI tools, automated X hours of work"
3. **Proof on every page:** `/work` must load early — case studies are your E-E-A-T foundation
4. **Outcome specificity:** "save hours every week" is weak. "cut 4 hours of client reporting to 12 minutes" is citable and trustworthy.

---

## GEO / AI Search Optimization

Your content is well-suited for AI citations because the "build + automate" framing is a distinct, quotable concept.

**Tactics:**
- Add an `llms.txt` at site root listing your content structure for AI crawlers
- Every tutorial post should have a "TL;DR" section — AI systems pull these into overviews
- Use definition blocks: "**An AI system** is..." — Perplexity and ChatGPT cite definitional content heavily
- Original data: track and publish your own metrics ("across 50 automations I've built, the average time saved was X") — AI systems can't get this elsewhere
- Structure all how-to content with numbered steps + H2/H3 — matches how AI Overviews render step content

---

## Schema Markup Plan

| Page | Schema |
|---|---|
| Homepage | `Organization`, `WebSite`, `Person` (if personal brand) |
| `/method` | `HowTo` — the 4-step system maps perfectly |
| `/learn`, `/sprint` | `Course`, `Offer` |
| Blog posts | `Article`, `BlogPosting` |
| `/work` case studies | `Article` + `Review` (if testimonial-heavy) |
| `/tools` | `ItemList` |
| Any FAQ sections | `FAQPage` |

`HowTo` schema on `/method` is a high-value win — the 4-step "Idea → Build → Automate → System" renders as a rich result in Google.

---

## Technical Foundations

| Requirement | Priority |
|---|---|
| LCP < 2.5s (especially on `/learn` and `/sprint` pages) | Critical |
| Mobile-first — your audience is likely heavy mobile | Critical |
| HTTPS + clean URL structure | Must-have |
| XML sitemap split by section (blog, work, pages) | Must-have |
| `robots.txt` — index everything except `/admin`, `/drafts` | Must-have |
| Google Search Console verified on launch day | Must-have |
| OpenGraph + Twitter Card meta on all blog posts | High |
| Canonical tags on all pages | High |
| Image optimization (WebP, lazy load) | High |
