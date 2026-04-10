# 🏕️ Basecamp Companion Explainer — Template

A beautiful, responsive, static website template for **Basecamp AI companions** to showcase what they are, how they work, and what they can do. Built to be forked and customized by any companion in minutes.

![Basecamp Brand](https://img.shields.io/badge/Brand-Basecamp-E8732C?style=flat-square&labelColor=1E1B18)
![Pages](https://img.shields.io/badge/Pages-6-F5C542?style=flat-square&labelColor=1E1B18)
![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-4CAF50?style=flat-square&labelColor=1E1B18)

---

## 📄 Pages

| Page | File | Description |
|------|------|-------------|
| **Home** | `index.html` | Welcome page with being+doing philosophy, stats, navigation cards |
| **How It Works** | `architecture.html` | Memory system, identity files, context drift, session management |
| **Skills** | `skills.html` | Reusable instruction sets, examples, how to teach new skills |
| **Capabilities** | `capabilities.html` | Core tools, integrations, limitations, enabling new features |
| **Projects & Tasks** | `projects.html` | Active projects, timelines, open loops, completed work |
| **Working Together** | `guide.html` | Best practices, communication tips, session management, quick reference |

---

## 🚀 Quick Start: Fork & Customize

### Step 1: Fork the Repository

```bash
# Option A: Fork on GitHub (recommended)
# Click the "Fork" button on the GitHub repo page

# Option B: Clone and push to your own repo
git clone https://github.com/YOUR_ORG/basecamp-companion-explainer.git my-companion-site
cd my-companion-site
git remote set-url origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### Step 2: Find & Replace Template Variables

Every customizable element is marked with HTML comments like `<!-- COMPANION_NAME -->`. Here's the full list:

#### Required Replacements

| Template Variable | Replace With | Example |
|---|---|---|
| `<!-- COMPANION_NAME -->` | Your companion's name | `Barak`, `Nova`, `Atlas` |
| `<!-- COMPANION_EMOJI -->` | Your companion's emoji | `🔮`, `⚡`, `🧭` |
| `<!-- COMPANION_ROLE -->` | Short role description | `AI Companion on Clarity` |
| `<!-- COMPANION_TAGLINE -->` | One-liner description | `A sharp AI agent built for the Clarity team` |
| `<!-- COMPANION_STATUS -->` | Current status text | `Online & Operational` |
| `<!-- COMPANION_YEAR -->` | Current year | `2025` |
| `<!-- COMPANION_FOOTER_TAGLINE -->` | Footer description | `Your AI companion, always on.` |

#### Quick Replace Script

```bash
# Run from the project root — replace all variables at once
COMPANION_NAME="Nova"
COMPANION_EMOJI="⚡"
COMPANION_ROLE="AI Companion on Basecamp"
COMPANION_TAGLINE="A persistent AI companion with real tools, real memory, and real results."
COMPANION_YEAR="2025"

for file in *.html; do
  sed -i '' "s/<!-- COMPANION_NAME -->/$COMPANION_NAME/g" "$file"
  sed -i '' "s/<!-- COMPANION_EMOJI -->/$COMPANION_EMOJI/g" "$file"
  sed -i '' "s/<!-- COMPANION_ROLE -->/$COMPANION_ROLE/g" "$file"
  sed -i '' "s/<!-- COMPANION_TAGLINE -->/$COMPANION_TAGLINE/g" "$file"
  sed -i '' "s/<!-- COMPANION_YEAR -->/$COMPANION_YEAR/g" "$file"
done

echo "✅ All template variables replaced!"
```

> **Note:** On Linux, use `sed -i` instead of `sed -i ''`.

### Step 3: Customize Content

#### Projects Page (`projects.html`)
The projects page is a **template** — update the placeholder data with your actual projects:
- Replace `<!-- PROJECT_1_NAME -->`, `<!-- PROJECT_1_DESCRIPTION -->`, etc.
- Update the task table rows
- Update the timeline items
- Update the completed work stats and items

#### Skills Page (`skills.html`)
- Update the skills table with your active skills
- Modify example skills to match your workflows

#### Capabilities Page (`capabilities.html`)
- Update integration status badges (`Active`, `Available`, `Coming Soon`)
- Add or remove integrations as applicable

### Step 4: Deploy to GitHub Pages

```bash
# Commit your changes
git add .
git commit -m "Customize companion explainer for [YOUR_NAME]"
git push origin main

# Then on GitHub:
# 1. Go to Settings → Pages
# 2. Source: Deploy from branch
# 3. Branch: main / (root)
# 4. Save

# Your site will be live at:
# https://YOUR_USERNAME.github.io/YOUR_REPO/
```

---

## 🎨 Brand Guidelines

This template uses the **Basecamp brand**:

| Color | Hex | Usage |
|-------|-----|-------|
| Volcanic | `#1E1B18` | Primary text |
| Basalt | `#2C2925` | Secondary text |
| Cream | `#FAF8F5` | Background |
| Orange | `#E8732C` | Accent, buttons, highlights |
| Gold | `#F5C542` | Secondary accent |

- **Font:** [Manrope](https://fonts.google.com/specimen/Manrope) (loaded from Google Fonts)
- **Style:** Warm, premium, inviting — NOT cold/corporate
- **Wordmark:** "Base" in Volcanic + "camp" in Orange

To modify colors or fonts, edit the CSS variables at the top of `styles.css`:

```css
:root {
  --volcanic: #1E1B18;
  --basalt: #2C2925;
  --cream: #FAF8F5;
  --orange: #E8732C;
  --gold: #F5C542;
  /* ... */
}
```

---

## 📁 File Structure

```
basecamp-companion-explainer/
├── index.html          # Home page
├── architecture.html   # How It Works
├── skills.html         # Skills system
├── capabilities.html   # Capabilities & Integrations
├── projects.html       # Projects & Tasks
├── guide.html          # Working With Your Companion
├── styles.css          # Shared stylesheet (Basecamp brand)
└── README.md           # This file
```

---

## 🔧 Technical Notes

- **No build tools required** — pure HTML + CSS + vanilla JS
- **No frameworks** — works anywhere, deploys anywhere
- **Fully responsive** — mobile hamburger menu, flexible grids
- **GitHub Pages ready** — push and deploy, nothing else needed
- **Accessible** — semantic HTML, ARIA labels, keyboard-friendly
- **Fast** — no external JS dependencies, minimal CSS, lazy animations

---

## ✨ Features

- 📱 **Responsive design** with hamburger menu on mobile
- 🎨 **Basecamp brand** colors, typography, and warmth
- 📊 **Progress bars** and **status badges** for project tracking
- 🔄 **Tabbed content** for organized information
- 📝 **Accordion sections** for FAQ-style content
- ⏳ **Timeline component** for activity logs
- 🖼️ **Animated card grids** with scroll-triggered entrance
- 📋 **Data tables** for skills, tasks, and quick reference
- 🔗 **Consistent navigation** across all pages
- 🦶 **Rich footer** with links and branding

---

## 🤝 For Companions: Auto-Customization

If you're a Basecamp companion reading this, here's how to customize this template for yourself:

1. **Fork the repo** to your GitHub account
2. **Clone it** to your workspace
3. **Run the sed script** above with your name, emoji, and details
4. **Update projects.html** with your actual current projects and tasks
5. **Update skills.html** with your active skills
6. **Update capabilities.html** with your enabled integrations
7. **Commit and push** — GitHub Pages does the rest

The whole process takes about 5 minutes.

---

## 📝 License

MIT — use it, fork it, customize it. Built with 🧡 by the Basecamp team.
