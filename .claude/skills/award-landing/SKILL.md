---
name: award-landing
description: Generate premium, award-gallery-inspired landing pages. Use when creating a new marketing landing page, redesigning a site with high-end aesthetics, or when the user mentions Awwwards, FWA, or "award-winning design."
disable-model-invocation: true
allowed-tools: Read, Write, Glob, Grep, Bash(mkdir:*), Bash(cp:*)
---

# Award-Winning Landing Page Director

Generate premium landing pages inspired by Awwwards/FWA galleries. This skill produces a complete creative direction package and a working Next.js scaffold.

## Quick Start

```
/award-landing "Brief describing the brand, product, and desired vibe"
```

---

## Workflow (7 Steps)

1. **Ingest Brief** — Parse brand, audience, vibe, constraints. Match against Reference Corpus + Style Clusters.
2. **DIRECTION.md** — Creative direction (template in Section 5)
3. **MOTION.md** — Motion system (patterns in Section 4)
4. **ASSETS.md** — Asset requirements (template in Section 5)
5. **PAGE_PLAN.md** — Page structure (template in Section 5)
6. **TOKENS.json** — Design tokens for CSS
7. **Code Scaffold** — Next.js project (Section 6)

---

## 1. Style Vocabulary

### Primary Vibes (Pick 1 Primary + 1 Secondary)
| Vibe | Definition |
|------|------------|
| `cinematic` | Dramatic scale, hero video/imagery, theatrical reveals |
| `editorial` | Magazine-inspired, strong typography hierarchy, content-first |
| `playful` | Bright colors, bouncy motion, whimsical illustrations |
| `brutal` | Raw, exposed structure, monospace type, anti-design |
| `minimal` | Maximum whitespace, restrained palette, surgical precision |
| `luxury` | Rich textures, gold/champagne accents, slow elegance |
| `futuristic` | Gradients, glassmorphism, tech-forward aesthetics |
| `artisanal` | Hand-crafted feel, organic textures, warm and human |
| `bold` | Oversized type, high contrast, unapologetic presence |
| `ethereal` | Soft gradients, floating elements, dreamlike atmosphere |

### Motion Regimes
| Regime | Description | GSAP Pattern |
|--------|-------------|--------------|
| `subtle` | Micro-interactions only | Fade, slight translate (20px max) |
| `kinetic-type` | Typography as motion | SplitText, character stagger |
| `scroll-scene` | Scroll-driven reveals | ScrollTrigger scrub, pin |
| `immersive` | Full takeover moments | Timeline sequences, morphs |
| `parallax` | Layered depth | Multiple speed layers |
| `mixed` | Playful variety | Bouncy eases, stagger, scale pops |
| `cursor-led` | Cursor drives motion | Mouse position tracking, magnetic effects |
| `minimal-motion` | Near-static, content-first | Instant or 100ms fades only |

### Materiality
| Label | Characteristics |
|-------|-----------------|
| `glass` | Backdrop blur, transparency, frosted surfaces |
| `paper` | Subtle shadows, layered cards, tactile depth |
| `metal` | Gradients, reflections, brushed textures |
| `fabric` | Soft edges, organic curves, textile patterns |
| `neon` | Glows, saturated colors, dark backgrounds |
| `organic` | Natural textures, earth tones, imperfect edges |

---

## 2. Style Clusters

### minimal-saas
Clean, restrained product pages. Geometric sans, neutral + single accent, subtle motion.
- **Exemplars:** Linear, Raycast, Cron Calendar, Height

### cinematic-hero
Film-inspired with immersive imagery, dramatic reveals, dark dominant.
- **Exemplars:** Studio Santi, Locomotive, Fantasy, Porsche

### editorial-magazine
Magazine layouts, strong type hierarchy, content-first, serifs + sans.
- **Exemplars:** Pentagram, Squarespace, Readymag, Cargo

### playful-brand
Vibrant, personality-driven, bold colors, unexpected interactions.
- **Exemplars:** Figma, Arc Browser, Mailchimp, Glossier

### futuristic-tech
Gradients, glass effects, 3D, neon accents on dark.
- **Exemplars:** Vercel, Framer, Nothing, Spotify

### luxury-premium
Refined, premium, elegant serifs, muted palette, slow motion.
- **Exemplars:** Superhuman, Bang & Olufsen, Aesop

### brutal-raw
Stark, exposed, monospace, black/white dominant.
- **Exemplars:** Pentagram, Sagmeister Walsh

### artisanal-craft
Handmade, organic textures, warm palettes, humanist type.
- **Exemplars:** Craft, Analogue, Allbirds, Patagonia

### experimental-art
Boundary-pushing, unusual layouts, generative, cursor-led.
- **Exemplars:** Sagmeister Walsh, Resn, Teenage Engineering

### product-hero
Product-centric with feature-benefit structure, conversion-optimized.
- **Exemplars:** Apple, Sonos, Tesla, Rivian

### agency-portfolio
Case study focus, distinctive display type, work-forward.
- **Exemplars:** Studio Santi, Basic Agency, Locomotive, Fantasy

---

## 3. Reference Corpus — Awwwards SOTM Winners

### Recent Winners (2024-2025)
| Site | Studio | Tags | Signature Technique |
|------|--------|------|---------------------|
| MindMarket | Louis Paquet | cinematic, experimental | WebGL particle morphing on scroll |
| Lando Norris | OFF+BRAND | cinematic, product-hero | Full-bleed video with kinetic type |
| Ponpon Mania | Patrick Heng | playful, experimental | 3D candy physics with cursor |
| Terminal Industries | REJOUICE | minimal, technical | ASCII art hero |
| Cartier Watches & Wonders | Immersive Garden | luxury, cinematic | Light ray product reveal |
| Tracing Art | Resn | experimental, artisanal | Generative brush strokes |
| Montfort | Immersive Garden | luxury, cinematic | Horizontal scroll with depth |
| Navigate | Resn | experimental, futuristic | 3D globe data visualization |
| Siena Film Foundation | Niccolò Miranda | editorial, cinematic | Paper-fold transitions |
| Dropbox Brand | Daybreak Studio | playful, editorial | Modular grid micro-animations |
| Immersive Garden | Immersive Garden | agency-portfolio | Case study depth parallax |
| Zentry | Resn | futuristic, experimental | Gaming HUD interface |
| Igloo Inc (SOTY) | abeto | minimal, luxury | Seamless shared-element transitions |
| Slosh Seltzer | Active Theory | playful, product-hero | Liquid physics simulation |
| Active Theory V6 | Active Theory | agency-portfolio | WebGL scene transitions |
| The Fabulous Cartier Journey | Merci Michel | luxury, cinematic | 360° WebGL jewelry viewer |

### Classic Winners (2020-2023)
| Site | Studio | Tags | Signature Technique |
|------|--------|------|---------------------|
| Lusion v3 (SOTY) | Lusion | experimental, futuristic | WebGL fluid mouse distortion |
| Locomotive® | Locomotive | agency-portfolio | Smooth scroll + horizontal sections |
| The Hall of Zero Limits | Dogstudio | cinematic, experimental | Scroll-driven 3D environment |
| Bruno Simon Portfolio (SOTY) | Bruno Simon | experimental, playful | 3D car driving on terrain |
| Persepolis Reimagined (SOTY) | Monks | cinematic, experimental | Historical 3D reconstruction |
| Apple AirPods Pro | Apple | minimal, product-hero | Scroll-driven product rotation |
| 20 Years of Xbox Museum | Active Theory | cinematic, playful | 3D museum walkthrough |

---

## 4. Motion Patterns Reference

Key GSAP patterns. Use pattern name + signature as implementation guide.

| Pattern | Use Case | Key GSAP Signature |
|---------|----------|-------------------|
| **Lenis Smooth Scroll** | Buttery scroll | `new Lenis({ duration: 1.2, smoothWheel: true })` → bridge with `lenis.on("scroll", ScrollTrigger.update)` |
| **SplitText Characters** | Kinetic headlines | `new SplitText(el, { type: "chars" })` then `gsap.from(split.chars, { opacity: 0, y: 50, stagger: 0.02 })` |
| **ScrollTrigger Pin** | Scroll-driven reveals | `scrollTrigger: { trigger, pin: true, scrub: 1, start: "top top", end: "+=200%" }` |
| **Parallax Layers** | Multi-speed depth | `gsap.to(".layer", { yPercent: -30, scrollTrigger: { scrub: true } })` — vary per layer |
| **Magnetic Button** | Cursor-led CTA | Track mouse relative to center, `gsap.to(btn, { x: dx*0.3, y: dy*0.3 })`, reset with `elastic.out(1, 0.3)` |
| **Clip-Path Reveal** | Text wipe entrance | `gsap.fromTo(el, { clipPath: "polygon(0 0, 0 0, 0 100%, 0 100%)" }, { clipPath: "polygon(0 0, 100% 0, 100% 100%, 0 100%)" })` |
| **Image Reveal** | Dramatic image entrance | Wrapper `overflow: hidden`, image `gsap.from({ yPercent: 100, scale: 1.4 })` |
| **Horizontal Scroll** | Galleries | `gsap.to(panels, { xPercent: -100*(n-1), scrollTrigger: { pin: true, scrub: 1, snap: 1/(n-1) } })` |
| **Infinite Marquee** | Scrolling text/logos | Clone content, `gsap.to(el, { x: -width/2, duration: width/speed, repeat: -1, ease: "none" })` |
| **Scroll Video** | Apple-style reveals | `video.currentTime = scrollProgress * video.duration` via ScrollTrigger onUpdate |
| **Custom Cursor** | Signature cursor | Two elements: cursor (0.1s), follower (0.5s), scale on hover |
| **Preloader Exit** | Branded loading | Timeline: logo in → progress fill → logo out → container `yPercent: -100` |
| **Page Transitions** | Cross-page | `next-view-transitions` package or native `document.startViewTransition()` |

> **SplitText Note:** SplitText requires Club GSAP. Free alternative: manually split text into `<span class="char">` elements.

### Reduced Motion
All patterns MUST check `prefers-reduced-motion`. Replace animations with instant state, keep opacity fades only.

---

## 4.5. Modern CSS Reference

| Technique | Support | Key Syntax |
|-----------|---------|------------|
| **View Transitions API** | Chrome 111+, Safari 18+ | `document.startViewTransition()`, `::view-transition-old/new(root)` |
| **CSS Scroll-Timeline** | Chrome 115+ | `animation-timeline: scroll()`, `animation-range: entry 0% cover 40%` |
| **Container Queries** | All modern | `container-type: inline-size`, `@container (min-width: 400px)`, units: `cqi` |
| **Variable Font Animation** | All modern | `font-variation-settings: 'wght' 400`, transition on hover/scroll |
| **AVIF Images** | Chrome, Firefox, Safari 16+ | `<source srcset=".avif" type="image/avif">` in `<picture>` |
| **color-mix()** | All modern | `color-mix(in srgb, var(--color), white 20%)` for dynamic tints |

---

## 5. Artifact Templates

### DIRECTION.md Template

```markdown
# Creative Direction: [Project Name]

## Design Thesis
> One sentence capturing the essence.

## Mood Triad
1. **[Adjective 1]** — How it manifests
2. **[Adjective 2]** — How it manifests
3. **[Adjective 3]** — How it manifests

## Style Classification
- **Primary Vibe:** [from vocabulary]
- **Secondary Vibe:** [from vocabulary]
- **Cluster:** [from clusters]
- **Motion Regime:** [from vocabulary]
- **Materiality:** [from vocabulary]

## Color Philosophy
| Role | Hex | Rationale |
|------|-----|-----------|
| Background | #hex | Why |
| Foreground | #hex | Why |
| Accent | #hex | Why |
| Neutral 0-5 | #hex | Scale from dark to light |

## Typography System
| Role | Font | Weight | Usage |
|------|------|--------|-------|
| Display | [font] | [weight] | Headlines |
| Body | [font] | [weight] | Paragraphs |
| Mono | [font] | [weight] | Code/data |

## Reference DNA
| Site | What to Borrow |
|------|---------------|
| [Site 1] | Specific element |
| [Site 2] | Specific element |
```

#### Completed Example: Maison Horologique

```markdown
# Creative Direction: Maison Horologique

## Design Thesis
> Timeless precision meets digital craft — a website that moves with the deliberate elegance of fine watchmaking.

## Mood Triad
1. **Precise** — Every element aligned to 8px grid; typography set with Swiss accuracy
2. **Luxurious** — Deep blacks, warm golds, generous whitespace; materials that suggest weight
3. **Unhurried** — Slow reveals reward patience; no aggressive CTAs; quiet confidence

## Style Classification
- **Primary Vibe:** luxury
- **Secondary Vibe:** cinematic
- **Cluster:** luxury-premium
- **Motion Regime:** scroll-scene
- **Materiality:** metal

## Color Philosophy
| Role | Hex | Rationale |
|------|-----|-----------|
| Background | #0C0B0A | Near-black with warm undertone, like onyx |
| Foreground | #F5F3EF | Warm white, not clinical |
| Accent | #C9A962 | Champagne gold, brand signature |
| Neutral 0 | #0C0B0A | Deepest shadow |
| Neutral 1 | #1A1918 | Card backgrounds |
| Neutral 2 | #2D2B29 | Borders |
| Neutral 3 | #524F4B | Muted text |
| Neutral 4 | #8A8580 | Secondary text |
| Neutral 5 | #C4BFB8 | Tertiary |

## Typography System
| Role | Font | Weight | Usage |
|------|------|--------|-------|
| Display | Cormorant Garamond | 300, 400 | Headlines — elegant serif |
| Body | Inter | 400, 500 | Paragraphs — clean |
| Mono | JetBrains Mono | 400 | Model numbers |

## Reference DNA
| Site | What to Borrow |
|------|---------------|
| Cartier Watches & Wonders | Light ray product reveals |
| Bang & Olufsen | Product photography as hero |
| Igloo Inc | Seamless section transitions |
```

### MOTION.md Template

```markdown
# Motion System: [Project Name]

## Motion Philosophy
> One sentence on motion's role.

## Regime: [regime-name]

## Timing Tokens
| Token | Value | Usage |
|-------|-------|-------|
| `--duration-fast` | 150ms | Hovers |
| `--duration-normal` | 300ms | Transitions |
| `--duration-slow` | 500ms | Reveals |

## Easing Tokens
| Token | Value | Usage |
|-------|-------|-------|
| `--ease-out` | cubic-bezier(0, 0, 0.2, 1) | Entrances |
| `--ease-in-out` | cubic-bezier(0.4, 0, 0.2, 1) | State changes |

## GSAP Patterns
[Key patterns from Section 4 with project-specific values]

## Signature Interaction
[One unique interaction for this project]

## Reduced Motion
All animations respect `prefers-reduced-motion`. Replace with instant states, keep opacity fades.
```

#### Completed Example: Maison Horologique

```markdown
# Motion System: Maison Horologique

## Motion Philosophy
> Motion should feel like the sweep of a second hand — precise, unhurried, mechanically perfect.

## Regime: scroll-scene

## Timing Tokens
| Token | Value | Usage |
|-------|-------|-------|
| `--duration-fast` | 200ms | Button hovers |
| `--duration-normal` | 400ms | Icon transitions |
| `--duration-slow` | 800ms | Section entrances |
| `--duration-slower` | 1200ms | Hero reveals |

## Easing Tokens
| Token | Value | Usage |
|-------|-------|-------|
| `--ease-out` | cubic-bezier(0.16, 1, 0.3, 1) | Smooth entrances |
| `--ease-luxury` | cubic-bezier(0.19, 1, 0.22, 1) | Signature slow reveals |

## GSAP Patterns

**Hero Watch Reveal:**
```javascript
tl.from(".hero-watch", { opacity: 0, y: 100, scale: 0.95, duration: 1.5, ease: "power3.out" })
  .from(".hero-headline span", { opacity: 0, y: 40, stagger: 0.05 }, "-=0.8");
```

**Scroll-Pinned Product Rotation:**
```javascript
gsap.to(".product-360", { rotationY: 360, scrollTrigger: { trigger: ".product-section", pin: true, scrub: 1, end: "+=200%" } });
```

## Signature Interaction: Crown Rotation
On watch hover, crown rotates 45° as if being wound, elastic return on leave.

## Reduced Motion
Replace scroll-pinned with static layouts. Keep 0.3s opacity fades. Show static product image.
```

### ASSETS.md Template

```markdown
# Asset Requirements: [Project Name]

## Hero Media
- **Type:** [video/image/3D]
- **Dimensions:** [e.g., 3840x2160]
- **Format:** [MP4/WebM/WebP]
- **Mood:** [description]
- **Source:** [stock/custom/AI]

## Photography Style
- Treatment: [contrast, tones]
- Lighting: [natural/studio]
- Composition: [centered/asymmetric]

## Iconography
- **Style:** [outline/solid]
- **Source:** [Lucide/Heroicons/custom]

## Font Files
| Font | Weights | Source |
|------|---------|--------|
| [Display] | [weights] | [source] |
| [Body] | [weights] | [source] |

## Image Optimization
- Format: AVIF → WebP → JPEG
- Sizes: srcset 640, 960, 1280, 1920
- Lazy loading below fold
```

#### Completed Example: Maison Horologique

```markdown
# Asset Requirements: Maison Horologique

## Hero Media
- **Type:** Video (product reveal)
- **Dimensions:** 3840x2160 (4K)
- **Format:** MP4 (H.265), WebM fallback
- **Mood:** Cinematic slow-motion, watch emerging from darkness into warm light
- **Source:** Custom shoot — macro lens, controlled studio lighting

## Photography Style
- Treatment: High contrast, warm shadows, champagne highlights
- Lighting: Single key from upper-left, soft fill, dramatic falloff
- Composition: Product centered, generous negative space

## Iconography
- **Style:** Custom 1px line icons matching Cormorant letterforms
- **Icons:** Crown, movement, sapphire, water resistance, warranty

## Font Files
| Font | Weights | Source |
|------|---------|--------|
| Cormorant Garamond | 300, 400, 500 | Google Fonts |
| Inter | 400, 500 | Google Fonts |
| JetBrains Mono | 400 | Google Fonts |

## Image Optimization
- Format: AVIF → WebP → JPEG
- Sizes: srcset 640, 960, 1280, 1920, 2560
- Quality: 85% hero, 80% secondary
- Placeholder: Solid #0C0B0A
```

### PAGE_PLAN.md Template

```markdown
# Page Structure: [Project Name]

## Section Overview
| # | Section | Purpose | Layout |
|---|---------|---------|--------|
| 1 | Hero | Value prop | Full-bleed |
| 2 | [Name] | [Purpose] | [Layout] |
| ... | ... | ... | ... |
| N | Footer | Navigation, legal | Multi-column |

## Section Details
[For each section: Purpose, Content, Media, Animation]

## Component Inventory
| Component | Count | Variants |
|-----------|-------|----------|
| Button | [n] | primary, secondary, ghost |
| Card | [n] | [variants] |

## Responsive Strategy
| Breakpoint | Changes |
|------------|---------|
| Mobile <768px | Single column, stacked CTAs |
| Desktop >1024px | Full experience |
```

#### Completed Example: Maison Horologique

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

## Section Details

### Hero
- **Headline:** "Where Time Becomes Art"
- **Subhead:** "Swiss precision. Timeless elegance. Since 1892."
- **CTAs:** "Explore Collection" → #collection, "Book Appointment" → /boutiques
- **Media:** 4K video loop — watch emerging from shadow
- **Animation:** Hero Watch Reveal (from MOTION.md)

### Collection
- 4 product cards: image, family name, price, CTA
- Horizontal scroll with snap points

### Craftsmanship
- 4 features: Movement, Materials, Crystal, Water resistance
- Pinned scroll with sequential reveals

## Component Inventory
| Component | Count | Variants |
|-----------|-------|----------|
| Button | 8 | primary (gold), secondary (outline), ghost |
| Card | 6 | product, location |
| ProductImage | 4 | with hover zoom |

## Responsive Strategy
| Breakpoint | Changes |
|------------|---------|
| Mobile <768px | Single column, vertical collection, simplified map |
| Desktop >1024px | Full animations, horizontal scroll, 4-column footer |
```

### TOKENS.json Template

```json
{
  "colors": {
    "bg": "#0a0a0f",
    "fg": "#ffffff",
    "accent": "#3b82f6",
    "neutral": ["#12121a", "#1a1a24", "#2a2a36", "#4a4a58", "#6a6a78", "#8a8a98"]
  },
  "typography": {
    "fontSans": "Inter, system-ui, sans-serif",
    "fontDisplay": "Inter, system-ui, sans-serif",
    "fontMono": "JetBrains Mono, monospace"
  },
  "spacing": {
    "sectionY": "120px",
    "sectionYMobile": "80px",
    "maxWidth": "1200px"
  },
  "motion": {
    "durationFast": "150ms",
    "durationNormal": "300ms",
    "durationSlow": "500ms",
    "easeOut": "cubic-bezier(0, 0, 0.2, 1)",
    "easeInOut": "cubic-bezier(0.4, 0, 0.2, 1)"
  }
}
```

### QA.md Template

```markdown
# QA Checklist: [Project Name]

## Accessibility
- [ ] Contrast ≥ 4.5:1 text, ≥ 3:1 large text
- [ ] Alt text on images
- [ ] Visible focus states
- [ ] Skip link present
- [ ] `prefers-reduced-motion` respected
- [ ] Keyboard navigable

## Performance
- [ ] Lighthouse ≥ 90
- [ ] LCP < 2.5s, CLS < 0.1
- [ ] Images AVIF/WebP with srcset
- [ ] Below-fold lazy loaded
- [ ] JS bundle < 200KB gzipped

## Responsive
- [ ] 320px minimum supported
- [ ] Touch targets ≥ 44x44px
- [ ] 16px base font
```

---

## 6. Code Scaffold

### Stack
- **Next.js 14+** App Router
- **Tailwind CSS v4** with `@theme` directive
- **GSAP + @gsap/react + ScrollTrigger**
- **TypeScript** strict mode
- **Lenis** for smooth scroll (optional)
- **next-view-transitions** for page transitions (optional)

### Key Dependencies
```json
{
  "dependencies": {
    "next": "^14.2.0",
    "react": "^18.3.0",
    "gsap": "^3.12.5",
    "@gsap/react": "^2.1.1",
    "lenis": "^1.0.0"
  },
  "devDependencies": {
    "tailwindcss": "^4.0.0",
    "@tailwindcss/postcss": "^4.0.0",
    "typescript": "^5.6.0"
  }
}
```

### Tailwind v4 Theme
Inject TOKENS.json into `globals.css`:

```css
@import "tailwindcss";

@theme {
  --color-bg: #0a0a0f;
  --color-fg: #ffffff;
  --color-accent: #3b82f6;
  --color-neutral-0: #12121a;
  /* ... remaining tokens ... */
  
  --font-sans: Inter, system-ui, sans-serif;
  --font-display: /* display font */;
  
  --duration-fast: 150ms;
  --duration-slow: 500ms;
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
}
```

### Essential Patterns
- **Reduced Motion:** Always check `prefers-reduced-motion`
- **Skip Link:** `<a href="#main" class="skip-link">Skip to content</a>`
- **Dark/Light:** CSS variables with `.dark` class toggle, localStorage preference
- **GSAP Context:** Always use `gsap.context()` for React cleanup

---

## 7. Anti-Patterns

1. **Generic SaaS Templates** — No cookie-cutter hero + 3 features + pricing
2. **Motion for Motion's Sake** — Every animation must guide attention or provide feedback
3. **Ignoring Accessibility** — Reduced motion mandatory, contrast WCAG AA, skip links
4. **Stock Photo Overload** — Max 3-5, prefer illustration/3D/custom
5. **Typography Neglect** — Type is 80% of design, invest in hierarchy
6. **Scroll Hijacking** — Never break native scroll; scrub fine, takeover not
7. **Performance Ignorance** — LCP > 2.5s is failure

---

## 8. Output Checklist

Before completing, verify all artifacts exist:

- [ ] **DIRECTION.md** — Creative direction with thesis, colors, typography
- [ ] **MOTION.md** — Motion system with timing, easing, GSAP patterns
- [ ] **ASSETS.md** — Asset requirements and specifications
- [ ] **PAGE_PLAN.md** — Full page structure with sections
- [ ] **TOKENS.json** — Design tokens for CSS injection
- [ ] **QA.md** — Accessibility, performance checklist
- [ ] **Code scaffold** — Next.js project with tokens applied

Place all artifacts in: `runs/[project-name]-[timestamp]/`
