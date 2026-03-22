# Using Claude SEO Skills in Claude Code

A guide to installing and using the Claude SEO skill suite.

---

## Prerequisites

- [Claude Code](https://claude.ai/code) installed and running
- Python 3.10 or higher
- Git

Check your Python version:

```bash
python3 --version
```

If you're on Python 3.9 or lower, install a newer version before continuing.

---

## Install the Claude SEO Skill

```bash
git clone --depth 1 https://github.com/AgriciDaniel/claude-seo.git
bash claude-seo/install.sh
```

Restart Claude Code after installation.

---

## Available Skills

Once installed, these slash commands are available in Claude Code:

| Skill | Purpose |
|---|---|
| `/seo-plan` | Strategic SEO planning |
| `/seo-audit` | Full site audit |
| `/seo-technical` | Technical SEO audit |
| `/seo-content` | Content quality analysis |
| `/seo-page` | Single-page deep analysis |
| `/seo-schema` | Structured data audit and generation |
| `/seo-sitemap` | Sitemap validation and generation |
| `/seo-images` | Image optimization audit |
| `/seo-geo` | AI search optimization |

---

## How to Use

Run any skill by typing the slash command in Claude Code, optionally followed by a URL or context:

```
/seo-plan
/seo-audit https://yoursite.com
/seo-page https://yoursite.com/blog/post-slug
```

For `/seo-plan`, provide your business context — what the site does, who it's for, what you're selling — and the skill will generate a full strategy.

---

## Recommended Order

1. **Before building:** `/seo-plan` to define your strategy
2. **After site structure is live:** `/seo-technical` + `/seo-sitemap` + `/seo-schema`
3. **After core pages are live:** `/seo-page` on each key page
4. **After first batch of content:** `/seo-content` + `/seo-images` + `/seo-geo`
5. **Ongoing:** `/seo-audit` for a full health check, `/seo-page` before publishing new posts

---

## Persisting Your Plan

After running `/seo-plan`, save the output into a GitHub repo for reference:

```bash
mkdir my-seo-plan && cd my-seo-plan
git init
# paste your plan files here
git add . && git commit -m "Initial SEO plan"
gh repo create my-seo-plan --public --source . --remote origin --push
```

Install the GitHub CLI (`gh`) if needed:

```bash
# macOS
brew install gh

# no sudo / no Homebrew
curl -sS https://webi.sh/gh | sh
source ~/.config/envman/PATH.env

gh auth login
```
