# Award-Winning Landing Page Skill

A Claude Code skill for generating Awwwards-quality landing pages.

## What It Does

Given a brief, Claude generates a landing page that could win Site of the Day. Not "nice" — award-winning.

The skill teaches Claude **design taste**: how to develop a singular concept, create signature moments, wield restraint for impact, and self-evaluate whether output is truly exceptional.

## Installation

Copy the skill folder to your Claude Code project:

```bash
# Clone this repo
git clone https://github.com/your-username/award-winning-website-skill.git

# Copy to your project's .claude/skills/
cp -r award-winning-website-skill/.claude/skills/award-landing your-project/.claude/skills/
```

Or install globally (available in all projects):

```bash
cp -r .claude/skills/award-landing ~/.claude/skills/
```

## Usage

Just describe what you want:

```
"Build a landing page for a Swiss watch brand — luxury, timeless, precision"
```

```
"Create a site for a developer productivity tool called Flux"
```

```
"I need a playful landing page for a fitness app that gamifies workouts"
```

Claude will:
1. Develop a concept from your brief
2. Select appropriate vibes, clusters, and references
3. Design a signature moment
4. Generate complete Next.js code

## The 4-Phase Process

### Phase 1: Concept Extraction
- What's the single truth about this brand?
- What metaphor embodies it?
- What feeling persists after the user leaves?
- What's the signature moment?

### Phase 2: Vocabulary Selection
- Primary + secondary vibe (from 12 options)
- Motion regime
- Materiality
- Style cluster
- Reference DNA (2-3 Awwwards sites)

### Phase 3: Hierarchy Decisions
1. Typography (80% of visual impact)
2. Layout rhythm
3. Color restraint
4. Motion philosophy
5. Signature moment

### Phase 4: Self-Evaluation
- Can I describe the concept in 5 words?
- Is there ONE moment users will screenshot?
- Would every element survive "does this serve the concept?"

## Skill Structure

```
.claude/skills/award-landing/
├── SKILL.md                 # Main entry point (208 lines)
├── concepts/
│   ├── THESIS.md            # Developing singular concepts
│   ├── SIGNATURE.md         # Designing memorable moments
│   └── TENSION.md           # Restraint and surprise
├── taste/
│   ├── TYPOGRAPHY.md        # Type-first design thinking
│   └── EVALUATION.md        # Self-critique rubric
├── reference/
│   ├── VIBES.md             # 12 vibes + motion regimes
│   ├── CLUSTERS.md          # 12 style clusters
│   └── CORPUS.md            # 30+ Awwwards winners analyzed
└── examples/
    ├── MAISON.md            # Luxury watch brand
    ├── FLUX.md              # Developer tool
    └── BOUNCE.md            # Playful fitness app
```

## What Separates SOTD from "Good"

1. **Singular concept, relentless execution** — ONE thing done unforgettably
2. **Narrative choreography** — Motion directs attention through a story
3. **The Signature Moment™** — One interaction users remember and share
4. **Tension between restraint and surprise** — Quiet makes peaks land harder
5. **Typography as primary material** — Type IS the design
6. **Obsessive micro-details** — Every hover state is considered
7. **Speed as luxury** — Instant interactions, 60fps scroll

## Output

Claude generates:

| Artifact | Purpose |
|----------|---------|
| **DIRECTION.md** | Design thesis, colors, typography, references |
| **PAGE_PLAN.md** | Section structure, signature moment placement |
| **Code** | Complete Next.js 14+ project |

Tech stack:
- Next.js 14+ (App Router)
- Tailwind CSS
- GSAP + ScrollTrigger
- TypeScript

## Style Vocabulary

### 12 Vibes
`minimal` · `cinematic` · `editorial` · `playful` · `brutal` · `luxury` · `futuristic` · `artisanal` · `experimental` · `bold` · `ethereal` · `technical`

### 12 Clusters
| Cluster | Best For |
|---------|----------|
| minimal-saas | SaaS, dev tools, B2B |
| cinematic-hero | Entertainment, launches |
| editorial-magazine | Publications, agencies |
| playful-brand | Consumer apps, startups |
| futuristic-tech | Tech products, AI, crypto |
| luxury-premium | Fashion, hospitality, high-end |
| brutal-raw | Dev tools, manifestos |
| artisanal-craft | Sustainable brands, studios |
| experimental-art | Portfolios, art projects |
| technical-data | Enterprise, documentation |
| product-hero | Product launches, Apple-style |
| agency-portfolio | Creative agencies |

### Motion Regimes
`subtle` · `kinetic-type` · `scroll-scene` · `immersive` · `parallax` · `cursor-led` · `minimal-motion`

## Examples

See the [examples/](/.claude/skills/award-landing/examples/) folder for complete worked examples:

- **Maison Horologique** — Luxury Swiss watch brand with scroll-driven rotation
- **Flux** — Developer productivity tool with fluid task physics
- **Bounce** — Playful fitness app with bouncy cursor interactions

## License

MIT
