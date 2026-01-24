# Award-Winning Landing Page Skill

A Claude Code skill for generating premium, award-gallery-inspired landing pages.

## Quick Start

```bash
# In Claude Code, invoke the skill:
/award-landing "Brief describing your brand, product, and desired vibe"
```

## What This Skill Does

Given a user brief, generates a complete creative direction package:

1. **DIRECTION.md** — Design thesis, mood, colors, typography, references
2. **MOTION.md** — Motion system with GSAP patterns and timing
3. **ASSETS.md** — Asset requirements and specifications
4. **PAGE_PLAN.md** — Page structure with sections and components
5. **TOKENS.json** — Design tokens for code injection
6. **QA.md** — Accessibility and performance checklist
7. **Code Scaffold** — Working Next.js + Tailwind + GSAP project

## Installation

Copy this skill to your Claude Code skills directory:

```bash
# Personal skills (available in all projects)
cp -r .claude/skills/award-landing ~/.claude/skills/

# Or keep it as a project skill (this repo only)
# Already in .claude/skills/award-landing/
```

## Directory Structure

```
.claude/skills/award-landing/
├── SKILL.md                    # Main skill instructions
└── taxonomy/
    └── style_taxonomy.yaml     # 12 style cluster definitions
```

> Planned additions: corpus dataset, Next.js scaffold template, and example output (see Roadmap).

## Style Clusters

| Cluster | Description |
|---------|-------------|
| `minimal-saas` | Clean sans-serif, blue/purple accents, card-based |
| `cinematic-hero` | Full-bleed video, dramatic type, slow fades |
| `editorial-magazine` | Serif headlines, asymmetric grids |
| `playful-brand` | Rounded shapes, bouncy animations, bright colors |
| `futuristic-tech` | Gradients, blur effects, dark mode |
| `luxury-premium` | Thin serifs, gold accents, generous whitespace |
| `brutal-raw` | Monospace, exposed grid, anti-aesthetic |
| `artisanal-craft` | Hand-drawn elements, warm colors |
| `experimental-art` | Rule-breaking, unusual interactions |
| `technical-data` | Data viz, precise grids |
| `product-hero` | Hero product shot, minimal UI |
| `agency-portfolio` | Case study focus, horizontal scroll |

## Tech Stack (Generated Scaffold)

- **Next.js 14+** with App Router
- **Tailwind CSS v4** with `@theme` directive for tokens
- **GSAP + ScrollTrigger** for animations
- **TypeScript** strict mode
- **Accessibility** — reduced motion, skip links, WCAG AA contrast

## Example Output

Example artifact bundle + scaffold will be published after the template is finalized (tracked in Roadmap).

## Roadmap

1. **Corpus dataset** — compile `corpus/sites.csv` with the 50 referenced Awwwards winners.
2. **Machine-readable taxonomy** — export `taxonomy/clusters.json` for retrieval workflows.
3. **Code scaffold template** — add `templates/next-scaffold/` (Next.js + Tailwind + GSAP) referenced in SKILL.md.
4. **Demo output** — capture a complete run in `examples/demo-001/` for validation and onboarding.

## Non-Goals

- Not a general UI kit
- Not WebGL/Three.js (unless explicitly requested)
- Not for login/forms (keep those conventional)
- Not scraping the web (curated corpus only)

## License

MIT
