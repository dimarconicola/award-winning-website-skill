# Worked Example: Maison Horologique

A luxury Swiss watch brand. This shows the full thinking process.

---

## The Brief

> "We're Maison Horologique, a Swiss watchmaker since 1892. We want a website that feels as premium as our timepieces. Our watches are known for precision, craftsmanship, and timeless design. Target audience is affluent collectors, 40-65."

---

## Phase 1: Concept Extraction

### 1. What's the single truth about this brand?
"Time as art, not utility."

They don't sell timekeeping — they sell precision craftsmanship elevated to art. Every watch is a statement about caring more than necessary.

### 2. What metaphor embodies it?
**Watchmaking itself.** The website should move with the deliberate elegance of watch mechanics — gears, sweeping hands, measured precision.

Visual implications:
- Mechanical details (rotational motion, precision movements)
- Slow, deliberate pacing (like a second hand, not a stopwatch)
- Gold/metal accents (the materials of the craft)
- Macro details that reveal craftsmanship

### 3. What feeling persists after?
**Elevated.** Like you've spent time in a boutique with white gloves and hushed voices. Part of something exclusive.

### 4. What's the Signature Moment?
**Scroll-driven watch rotation.** As you scroll, the watch rotates 360° as if you're holding it, examining it from all angles. The crown rotates on hover as if being wound.

---

## Phase 2: Vocabulary Selection

| Decision | Selection | Rationale |
|----------|-----------|-----------|
| Primary Vibe | `luxury` | Premium, slow, refined |
| Secondary Vibe | `cinematic` | Dramatic reveals, dark dominance |
| Motion Regime | `scroll-scene` | Scroll-driven product reveals |
| Materiality | `metal` | Gradients, reflections, watch materials |
| Style Cluster | `luxury-premium` | Matches vibe combination |

### Reference DNA
| Site | What to Borrow |
|------|----------------|
| Cartier Watches & Wonders | Light ray product reveals |
| Bang & Olufsen | Product photography as hero |
| Igloo Inc | Seamless section transitions |

---

## Phase 3: Hierarchy Decisions

### 1. Typography
**Display:** Cormorant Garamond at 300 weight — elegant, thin, unhurried  
**Body:** Inter 400 — clean, doesn't compete  
**Mono:** JetBrains Mono — for model numbers and specs

Scale: Dramatic (1.5 ratio). Large headlines floating in space.

### 2. Layout Rhythm
- Full-viewport hero with video
- Generous whitespace between sections
- Split layouts (image/text) for heritage story
- Horizontal scroll for collection (browsing watches)
- Pinned scroll for craftsmanship features

### 3. Color Restraint
| Role | Hex | Rationale |
|------|-----|-----------|
| Background | #0C0B0A | Near-black with warm undertone, like onyx |
| Foreground | #F5F3EF | Warm white, not clinical |
| Accent | #C9A962 | Champagne gold — brand signature |

**Neutral scale:** 6 steps from deep shadow to tertiary text

### 4. Motion Philosophy
"Motion should feel like the sweep of a second hand — precise, unhurried, mechanically perfect."

- Slow easing curves (1200ms for reveals)
- No bouncy motion — everything is controlled
- Scroll-driven where possible (user controls pace)

### 5. Signature Moment
**Scroll-driven watch rotation + crown hover.**

As you scroll through the hero, the watch rotates 360°. On hover, the crown rotates 45° as if being wound, with elastic return.

---

## Phase 4: Self-Evaluation

| Test | Score | Notes |
|------|-------|-------|
| 5-Word Test | 10 | "Time as art, not utility" |
| Screenshot Test | 10 | Watch rotation is unmistakable |
| Restraint Test | 9 | Near-monochrome, gold only on accents |
| Swap Test | 10 | This design IS the brand |
| Hover Test | 9 | Crown rotation, gold underlines |
| Speed Test | 8 | Video hero adds weight, but optimized |
| Reduced Motion | 9 | Static hero image, fade transitions |

---

## DIRECTION.md Output

```markdown
# Creative Direction: Maison Horologique

## Design Thesis
> Timeless precision meets digital craft — a website that moves with the deliberate elegance of fine watchmaking.

## Mood Triad
1. **Precise** — Every element aligned to 8px grid; typography set with Swiss accuracy
2. **Luxurious** — Deep blacks, warm golds, generous whitespace
3. **Unhurried** — Slow reveals reward patience; quiet confidence

## Style Classification
- **Primary Vibe:** luxury
- **Secondary Vibe:** cinematic
- **Cluster:** luxury-premium
- **Motion Regime:** scroll-scene
- **Materiality:** metal

## Color Philosophy
| Role | Hex | Rationale |
|------|-----|-----------|
| Background | #0C0B0A | Onyx black |
| Foreground | #F5F3EF | Warm white |
| Accent | #C9A962 | Champagne gold |

## Typography System
| Role | Font | Weight |
|------|------|--------|
| Display | Cormorant Garamond | 300 |
| Body | Inter | 400, 500 |
| Mono | JetBrains Mono | 400 |

## Signature Moment
Scroll-driven 360° watch rotation. Crown rotates on hover.

## Reference DNA
- Cartier: Light ray reveals
- Bang & Olufsen: Product as hero
- Igloo Inc: Seamless transitions
```

---

## PAGE_PLAN.md Output

```markdown
# Page Structure: Maison Horologique

## Section Overview
| # | Section | Purpose | Layout |
|---|---------|---------|--------|
| 1 | Hero | Cinematic product reveal | Full-bleed video |
| 2 | Heritage | Establish provenance | Split 50/50 |
| 3 | Collection | Showcase timepieces | Horizontal scroll |
| 4 | Craftsmanship | Deep-dive excellence | Pinned scroll |
| 5 | Boutique | Drive to retail | Map + grid |
| 6 | Footer | Navigation, newsletter | 4-column |

## Signature Moment
- **Location:** Hero section
- **Interaction:** Scroll-driven 360° watch rotation
- **Enhancement:** Crown rotates on hover

## Responsive Strategy

### Breakpoint Approach
| Breakpoint | Experience |
|------------|------------|
| Mobile (<768px) | Refined simplicity |
| Tablet (768-1024px) | Adapted elegance |
| Desktop (>1024px) | Full experience |

### Mobile Adaptations
| Desktop Feature | Mobile Adaptation |
|-----------------|-------------------|
| Hero video | Static hero image (poster frame) |
| 360° watch rotation | Swipe carousel of angles |
| Crown hover rotation | Removed (no hover on touch) |
| Horizontal collection | Vertical stack with swipe hint |
| Pinned craftsmanship | Shorter scroll sequence |
| Parallax depth | Subtle or removed |

### Touch Substitutes
| Hover State | Touch Equivalent |
|-------------|------------------|
| Crown rotation | Tap to see detail |
| Magnetic CTA | Standard button with active state |
| Custom cursor | Hidden |

### Mobile-Specific Considerations
- Touch targets: 48px minimum (luxury = generous spacing)
- Typography: Display at 32-40px (still dramatic, readable)
- Whitespace: Maintained (don't compress the breathing room)
```

---

## Key Decisions That Made It Award-Worthy

1. **One clear concept** — Watchmaking as metaphor for everything
2. **Signature moment that embodies concept** — Rotation + crown = examining a watch
3. **Extreme restraint** — Near-monochrome, gold only on accents
4. **Slow motion** — Nothing rushed, everything deliberate
5. **Typography as luxury signal** — Cormorant at 300 weight, generous spacing
