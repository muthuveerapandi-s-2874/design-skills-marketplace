# 🎨 Design Skills Marketplace

> Build better UI. Faster. With AI.

An AI-powered **design intelligence layer** for Claude — enabling structured
thinking, scalable systems, and consistent visual design across products.

---

## ⚡ Why this exists

Design today is:

- ❌ Inconsistent across teams
- ❌ Hard to scale
- ❌ Dependent on individual thinking

**Design Skills Marketplace solves this by turning design expertise into
reusable, AI-powered skills.**

---

## 🧠 What you get

A modular set of Claude skills that help you:

- Think like a senior product designer
- Build scalable design systems
- Generate UI patterns and themes
- Standardize design decisions across teams

---

## 🎯 Core Skills

| Folder | Skill name | What it does |
|---|---|---|
| `skills/ui-thinking/` | `ui-design-thinking` | Bold, intentional UI direction-setting — pick a design stance before building. |
| `skills/design-lang/` | `ods-visual-language` | Apply Zoho's ODS visual language: composition, spacing, motion, palette, illustration. |
| `skills/zoho-theme-factory/` | `zoho-theme-factory` | 15 ODS-compliant themes (5 Brand + 10 Creative) for HTML, PPTX, DOCX, banners. |
| `skills/ods-design-system/` | `ods-design-system` | Enforces strict ODS token / component / theme usage from the local design system. |

---

## 🚀 Installation

### Option A — Claude Code plugin marketplace

```text
/plugin marketplace add muthuveerapandi-s-2874/design-skills-marketplace
/plugin install design-skills
```

### Option B — Clone directly
```bash
git clone https://github.com/muthuveerapandi-s-2874/design-skills-marketplace
```
Everything you need — skills, ODS tokens, components, themes — is in this single repo. No submodule setup needed.

---

## ⚙️ Usage

These skills **auto-activate** based on how you describe your task. There are
no slash commands — just describe what you want and Claude matches the right
skill from its description.

Example prompts that activate each skill:

- `ui-design-thinking` → *"Help me pick a bold design direction for this landing page."*
- `ods-visual-language` → *"Make this page feel premium and human using ODS."*
- `zoho-theme-factory` → *"Apply a warm Zoho theme to this deck."*
- `ods-design-system` → *"Build a dashboard UI using ODS tokens."*

---

## 🏗️ Architecture

```text
design-skills-marketplace/
├── .claude-plugin/
│   └── marketplace.json          # Plugin manifest
├── design-system/                # ODS design system (tokens, components, themes)
│   ├── DESIGN.md
│   ├── tokens/
│   ├── components/
│   ├── themes/
│   └── references/products/
├── skills/
│   ├── ui-thinking/SKILL.md
│   ├── design-lang/SKILL.md
│   ├── zoho-theme-factory/SKILL.md
│   └── ods-design-system/SKILL.md
├── .gitignore
├── .gitmodules
├── LICENSE
└── README.md
```

---

## 💼 Real-world use cases

**Designers** — structured UI thinking, faster decisions, consistent systems.
**Marketers** — landing page clarity, conversion-focused layouts.
**Startups** — build design systems fast, reduce reliance on large teams.
**Teams (Zoho-style workflows)** — standardize design language across products.

---

## 🔥 Vision

This is a foundation for:

- 🧠 AI-powered design systems
- 🏗️ Prompt-driven UI builders
- 🔄 Design → Code automation
- 🛡️ Brand consistency engines (BrandGuard)

---

## 🧩 Roadmap

- ✅ Core design skills
- 🔜 BrandGuard integration
- 🔜 Figma → AI workflows
- 🔜 Component generation engine
- 🔜 Design QA automation

---

## 👨‍💻 Creator

**Muthu** — Design × AI × Product Systems
GitHub: <https://github.com/muthuveerapandi-s-2874>

---

## 🤝 Contribute

Want to expand this system? You can add:

- New design skills
- UI frameworks
- Design tokens
- Automation workflows

See `CONTRIBUTING.md` (coming soon) for guidelines.

---

## ⭐ Support

If this helps your workflow, ⭐ the repo and share it with your team.

---

## 📜 License

MIT — see [LICENSE](./LICENSE).
