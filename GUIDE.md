# How to Build and Grow an SEO-Optimized Blog Using Claude Code

A complete guide to installing Claude SEO skills, creating a strategic SEO plan, building your blog, and auditing it at every stage.

---

## What This Guide Covers

1. Installing the Claude SEO skill suite
2. Creating a full SEO strategy before you build
3. Persisting your plan into a GitHub repo
4. Building your blog with SEO baked in from day one
5. Auditing at each stage using the right skill at the right time
6. Ongoing maintenance and improvement

---

## Prerequisites

- [Claude Code](https://claude.ai/code) installed and running
- Python 3.10 or higher
- Git

### Check your Python version

```bash
python3 --version
```

If you have Python 3.9 or lower, install a newer version via [python.org](https://www.python.org/downloads/) or your package manager before continuing.

---

## Step 1 — Install the Claude SEO Skill

The Claude SEO skill suite adds specialized SEO agents and slash commands to Claude Code.

```bash
git clone --depth 1 https://github.com/AgriciDaniel/claude-seo.git
bash claude-seo/install.sh
```

The installer will:
- Copy skill files to `~/.claude/skills/seo/`
- Install agent definitions to `~/.claude/agents/`
- Set up a Python virtual environment with required dependencies
- Optionally install Playwright for visual/screenshot analysis

Once installed, restart Claude Code. You'll have access to these slash commands:

| Skill | What it does |
|---|---|
| `/seo-plan` | Strategic SEO planning — keywords, architecture, content strategy, roadmap |
| `/seo-audit` | Full site audit — crawls up to 500 pages, 6 specialist sub-audits in parallel |
| `/seo-technical` | Technical audit — crawlability, Core Web Vitals, robots.txt, security headers |
| `/seo-content` | Content quality + E-E-A-T analysis |
| `/seo-page` | Deep single-page analysis |
| `/seo-schema` | Structured data detection, validation, and generation |
| `/seo-sitemap` | Sitemap validation and generation |
| `/seo-images` | Image optimization — alt text, WebP, lazy loading, CLS |
| `/seo-geo` | GEO / AI search optimization — AI Overviews, ChatGPT, Perplexity citations |

---

## Step 2 — Create Your SEO Strategy (Before Building Anything)

Before touching a CMS or writing a single post, run `/seo-plan` with your business context. This is the most important step — it shapes everything that follows.

In Claude Code, run:

```
/seo-plan
```

Then provide your business brief. Include:

- **Objective:** What the site sells or teaches
- **Core promise:** What transformation you deliver
- **Target audience:** Who they are and what pain they have
- **Positioning:** How you're different from competitors
- **Offers:** What you're selling (course, service, product, etc.)

The skill will generate:

- **Keyword strategy** — Tier 1 (own these first), Tier 2 (content/blog traffic), Tier 3 (AI search citations)
- **Competitive analysis** — who you're up against and where the white space is
- **Site architecture** — full URL hierarchy with pillar pages, blog categories, CTA paths
- **Content pillars** — topic clusters that build topical authority
- **E-E-A-T strategy** — how to build trust signals from day one
- **Schema plan** — which structured data goes on which page type
- **GEO plan** — how to get cited by AI Overviews, ChatGPT, and Perplexity
- **Technical checklist** — Core Web Vitals targets, mobile, indexing
- **KPI targets** — organic traffic, rankings, AI citations by month 3/6/12

---

## Step 3 — Persist Your Plan to GitHub

Once you have your strategy, save it into a version-controlled repo so it's always accessible and shareable.

If you don't have the GitHub CLI (`gh`), install it:

```bash
# macOS with Homebrew
brew install gh

# or via webi (no sudo required)
curl -sS https://webi.sh/gh | sh
source ~/.config/envman/PATH.env
```

Authenticate:

```bash
gh auth login
```

Create a local directory and commit your plan files:

```bash
mkdir my-seo-plan
cd my-seo-plan
git init
# Add your plan files here (SEO-STRATEGY.md, SITE-STRUCTURE.md, etc.)
git add .
git commit -m "Initial SEO strategy"
```

Create the GitHub repo and push:

```bash
gh repo create my-seo-plan --public --source . --remote origin --push
```

**Suggested files to include in your repo:**

| File | Contents |
|---|---|
| `README.md` | Overview of the site, positioning, core promise |
| `SEO-STRATEGY.md` | Keywords, competitors, E-E-A-T, GEO, schema plan |
| `SITE-STRUCTURE.md` | Full URL hierarchy, internal linking rules, page priorities |
| `CONTENT-CALENDAR.md` | Blog topics by pillar, target keywords, content types, weekly schedule |
| `IMPLEMENTATION-ROADMAP.md` | Phased action plan with KPI targets per phase |

---

## Step 4 — Build Your Site With SEO Baked In

### Architecture principles from your plan

- **Pillar pages first.** Create top-level pages for your main topic clusters before writing blog posts. These become the authority anchors everything else links back to.
- **Clean URL structure.** `/topic/subtopic/post-slug` — no dates, no IDs, no parameters.
- **One H1 per page.** It should match the primary keyword for that page.
- **CTA destination is a single URL.** Keeps conversion tracking clean.

### Internal linking rules (apply from post one)

1. Every blog post links back to its pillar page
2. Every blog post links to 1–2 related posts in the same category
3. Pillar pages link to all posts in their cluster
4. Pillar pages cross-link to each other — the combination is your product
5. Case studies link to your offer pages

### E-E-A-T from day one

- Author bio with specific, concrete credentials (not "AI expert" — "built X products, automated Y hours of work")
- Real screenshots, tool outputs, and before/after data in every post
- Outcome specificity: "12 minutes" beats "saves time"
- Case studies are your trust foundation — publish them before your offer pages

---

## Step 5 — Audit at Every Stage

Run the right skill at the right moment. Don't run a full audit before you have content, and don't skip the technical audit because you're focused on writing.

### Stage 1: Site structure is live, no content yet

```
/seo-technical
/seo-sitemap
/seo-schema
```

- `/seo-technical` — catches crawlability issues, HTTPS, robots.txt, redirect chains before Google indexes anything wrong
- `/seo-sitemap` — validates or generates your XML sitemap structure
- `/seo-schema` — sets up `Organization`, `WebSite`, and `Person` schema on homepage and about page

### Stage 2: Core pillar pages live (homepage, pillars, method, proof)

```
/seo-page [URL]   ← run on each pillar page
/seo-content
```

- `/seo-page` — deep analysis of title tag, H1, meta description, heading hierarchy, internal links, schema
- `/seo-content` — E-E-A-T check on your trust-anchor pages (proof/case study pages especially)

### Stage 3: First 8–10 blog posts published

```
/seo-content
/seo-page [URL]   ← on your top 2-3 posts
/seo-images
/seo-geo
```

- `/seo-content` — catches thin content across all posts before it hurts rankings
- `/seo-images` — alt text, WebP format, lazy loading, CLS prevention
- `/seo-geo` — AI crawler accessibility, llms.txt, passage-level citability

### Stage 4: ~20 posts, ~2 months in (first full audit)

```
/seo-audit
/seo-technical
/seo-schema
```

- `/seo-audit` — full site audit with health score; runs 6 specialist sub-audits in parallel across up to 500 pages
- `/seo-technical` — second pass now that you have real Core Web Vitals data to act on
- `/seo-schema` — validate `BlogPosting`, `HowTo`, `Course`, `ItemList` across the whole site

---

## Step 6 — Ongoing Maintenance

### Monthly

| Task | Skill |
|---|---|
| Audit each new post before publishing | `/seo-page [URL]` |
| Content quality check across the blog | `/seo-content` |
| Fix any new technical regressions | `/seo-technical` |

### Quarterly

| Task | Skill |
|---|---|
| Full site health score | `/seo-audit` |
| AI search visibility + llms.txt freshness | `/seo-geo` |
| Schema audit as new page types are added | `/seo-schema` |
| Refresh top-performing posts with new data | `/seo-content` |

---

## Publishing Cadence

**Minimum:** 2 posts/week to build topical authority in a reasonable timeframe
**Format rotation:** Tutorial → Case study → Explainer → Repeat
**Structure:** Alternate between your content pillars — don't publish 3 posts in one cluster then none in another

### Content that earns AI Overview citations

Write some posts in these formats specifically to get cited by AI search:

- **Direct question format:** "What is the fastest way to [X]?" — AI Overviews pull these
- **Definitional posts:** "What is [concept]?" — Perplexity and ChatGPT cite these heavily
- **FAQ format:** Include a clear TL;DR at the top of every tutorial
- **Step-by-step with numbered H2s:** Matches how AI Overviews render instructional content
- **Original data:** Anything you measured yourself that can't be found elsewhere

---

## The Full Sequence at a Glance

```
Install Claude SEO skill
    ↓
Run /seo-plan with your business brief
    ↓
Commit strategy to GitHub repo
    ↓
Build site structure (no content yet)
    → /seo-technical + /seo-sitemap + /seo-schema
        ↓
Build pillar pages
    → /seo-page (per page) + /seo-content
        ↓
Publish first 10 blog posts
    → /seo-content + /seo-images + /seo-geo
        ↓
Reach 20+ posts (~month 2)
    → /seo-audit (first full health score)
        ↓
Monthly: /seo-page on new posts + /seo-content
Quarterly: /seo-audit + /seo-geo + /seo-schema
```

---

## Tips

- **Don't skip the plan.** Running `/seo-plan` before building saves months of rework. Keyword intent shapes URL structure, which shapes internal linking, which shapes ranking potential.
- **Pillar pages before blog posts.** Posts link to pillar pages. If the pillar doesn't exist yet, that link juice has nowhere to go.
- **Case studies are your highest-leverage content.** They build E-E-A-T, convert visitors, and provide proof for every claim you make elsewhere on the site.
- **`/seo-page` before publishing is a habit, not a chore.** Catching a missing H1 or broken internal link before a post is indexed is infinitely easier than fixing it after.
- **AI search is early.** Running `/seo-geo` early and setting up `llms.txt` now puts you ahead of 95% of sites in your niche for AI Overview visibility.
