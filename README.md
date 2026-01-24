# Award-Winning Landing Page Skill

A Claude Code skill for generating premium, award-gallery-inspired landing pages.

## Quick Start

```bash
# In Claude Code, invoke the skill:
/award-landing "Brief describing your brand, product, and desired vibe"
```

## What This Skill Does

Given a brief, the skill:

1. **Parses vibes** — extracts 2-3 vibe keywords (e.g., "luxury", "minimal")
2. **Matches cluster** — uses vibe→cluster mapping to select a style cluster
3. **Pulls references** — finds 2-3 Awwwards SOTM sites with matching tags

Then generates:

| Artifact | Purpose |
|----------|---------|
| **DIRECTION.md** | Design thesis, mood, colors, typography, references |
| **MOTION.md** | Motion system with GSAP patterns and timing |
| **ASSETS.md** | Asset requirements and specifications |
| **PAGE_PLAN.md** | Page structure with sections and components |
| **TOKENS.json** | Design tokens for CSS injection |
| **QA.md** | Accessibility and performance checklist |

Output goes to: `runs/[project-name]-[timestamp]/`

## Installation

```bash
# Personal skills (available in all projects)
cp -r .claude/skills/award-landing ~/.claude/skills/

# Or keep as project skill (this repo only)
```

## Directory Structure

```
.claude/skills/award-landing/
├── SKILL.md                    # Main skill (~660 lines)
└── taxonomy/
    └── style_taxonomy.yaml     # 12 style cluster definitions
```

## Workflow

```
Brief → Extract Vibes → Match Cluster → Pull References
     → DIRECTION.md → MOTION.md → ASSETS.md → PAGE_PLAN.md
     → TOKENS.json → QA.md → User builds scaffold
```

**Example:** Brief "premium fintech dashboard for Gen Z" → vibes: `futuristic` + `minimal` → cluster: `futuristic-tech` → refs: Vercel, Zentry

## Style Vocabulary

### 12 Vibes
`cinematic` · `editorial` · `playful` · `brutal` · `minimal` · `luxury` · `futuristic` · `artisanal` · `technical` · `experimental` · `bold` · `ethereal`

### 12 Clusters
| Cluster | Vibes | Exemplars |
|---------|-------|-----------|
| `minimal-saas` | minimal + technical | Linear, Raycast, Height |
| `cinematic-hero` | cinematic + luxury | Studio Santi, Locomotive |
| `editorial-magazine` | editorial + minimal | Pentagram, Readymag |
| `playful-brand` | playful + bold | Figma, Arc Browser |
| `futuristic-tech` | futuristic + technical | Vercel, Framer |
| `luxury-premium` | luxury + minimal | Bang & Olufsen, Aesop |
| `brutal-raw` | brutal + minimal | Sagmeister Walsh |
| `artisanal-craft` | artisanal + editorial | Allbirds, Patagonia |
| `experimental-art` | experimental + bold | Resn, Teenage Engineering |
| `technical-data` | technical + minimal | Stripe, Webflow |
| `product-hero` | cinematic + minimal | Apple, Sonos, Tesla |
| `agency-portfolio` | bold + cinematic | Basic Agency, Fantasy |

### 8 Motion Regimes
`subtle` · `kinetic-type` · `scroll-scene` · `immersive` · `parallax` · `mixed` · `cursor-led` · `minimal-motion`

## Tech Stack (User Builds)

The skill generates direction + tokens. User must:

1. `npx create-next-app@latest [name] --typescript --tailwind --app`
2. `npm install gsap @gsap/react lenis`
3. Inject TOKENS.json into `globals.css` under `@theme { }`
4. Source assets per ASSETS.md
5. Run Lighthouse, test reduced motion

Stack:
- **Next.js 14+** App Router
- **Tailwind CSS v4** with `@theme` directive
- **GSAP + ScrollTrigger** for animations
- **TypeScript** strict mode

## Key Features

- **Vibe→Cluster Mapping** — deterministic style matching with fallback rules
- **Font Pairing Table** — 8 vibes mapped to Display/Body/Mono fonts
- **15 Reference Sites** — Awwwards SOTM winners with signature techniques
- **13 Motion Patterns** — GSAP signatures for common interactions
- **Completed Example** — "Maison Horologique" luxury watch brand

## Non-Goals

- Not a UI component library
- Not WebGL/Three.js (unless explicitly requested)
- Not production-ready code — direction + scaffold only
- Not scraping — curated corpus only

## License

MIT
