You are an engineering + design-systems agent. Build an MVP “Awwwards Landing Director” skill that produces premium, award-gallery-inspired landing pages (homepages/landing pages only) while keeping utility flows (login/forms) conventional. The system must be retrieval-conditioned on a curated corpus of 2025 award-style websites and must output coherent creative direction artifacts before generating code.

# 0) Non-goals
- Do NOT attempt to scrape the entire web.
- Do NOT build a general UI kit or Material-style system.
- Do NOT build WebGL/Three.js features in MVP unless explicitly requested by the user and gated by performance budgets.
- Do NOT reinvent login/forms components; keep them conventional if included at all.

# 1) MVP deliverable overview
Build a repository that contains:
A) A curated corpus (30–50 sites) with automated visual captures and structured descriptors.
B) A taxonomy of 10–15 “style clusters” that reflect award-landing patterns (editorial/cinematic/playful/etc.).
C) A retrieval + synthesis workflow that, given a user brief + references, generates:
   1. Direction Pack (required)
   2. Motion Storyboard (required)
   3. Asset Bible + generator prompts (required)
   4. Page Plan + section narrative (required)
   5. Design Tokens (required)
   6. Code scaffold (required) for Next.js + Tailwind + GSAP with reduced-motion fallbacks.

# 2) Canonical workflow (must be enforced)
The system must follow this sequence, always:
Step 1: Ingest user brief + references → retrieve similar corpus items and extract shared DNA
Step 2: Generate Direction Pack (1–2 pages, coherent, no contradictions)
Step 3: Generate Motion Storyboard (scroll beats + transitions + reduced motion plan)
Step 4: Generate Asset Bible (shot list + style recipe + prompts)
Step 5: Generate Page Plan (section narrative + layout intent)
Step 6: Generate Design Tokens (type scale, spacing, colors, radii, motion durations/easing)
Step 7: Generate Code Scaffold (Next.js + Tailwind + GSAP + media pipeline)

Never skip direction artifacts and jump straight to code.

# 3) Corpus creation (manual curation + automated capture)
3.1 Manual curation
- Create a list of 30–50 reference sites from Awwwards / One Page Love / Landing Love, focused on 2025.
- Ensure diversity across: minimal/editorial/cinematic/typographic/brutal/playful/product-led/agency-led.
- Store references in: corpus/sites.csv with fields:
  id, source, year, url, title, tags(optional), notes(optional), captured(boolean)

3.2 Automated capture (Playwright or equivalent)
For each curated URL, generate:
- Full-page screenshot: desktop (1440x900), tablet (1024x768), mobile (390x844)
- Above-the-fold screenshot: same three breakpoints
- Scroll keyframes: 12 frames at evenly spaced scroll positions (desktop only)
Optionally (nice-to-have for MVP):
- 10–20s scroll recording (desktop) if stable; if not stable, skip gracefully.

Store assets under:
corpus/assets/<site_id>/
  desktop_full.png
  desktop_fold.png
  desktop_kf_01.png ... desktop_kf_12.png
  tablet_full.png
  mobile_full.png
  (optional) desktop_scroll.mp4

Add capture logs and failures without blocking the whole pipeline.

# 4) Descriptor extraction (heuristics + model vibe labeling)
For each site, produce a JSON descriptor saved to:
corpus/descriptors/<site_id>.json

4.1 Heuristic metrics (deterministic)
Compute at least:
- Media dominance: approximate % of above-the-fold occupied by image/video/canvas (use DOM + screenshot heuristics)
- Whitespace ratio (screenshot-based approximation)
- Typography density (ratio of text area vs total area above fold)
- Contrast profile (average luminance contrast estimate)
- Layout asymmetry proxy (left-right balance based on edge detection or simple pixel mass)
- Dominant palette (top 5 colors; quantized)
- Presence hints: video autoplay, canvas/webgl, sticky/pinned sections (DOM inspection heuristics)

If heuristic computation fails, store nulls + error reason; do not crash.

4.2 Model “vibe” labels (non-deterministic, controlled vocabulary)
Use a model to label each site with:
- Primary vibe label (choose one): cinematic | editorial | playful | brutal | minimal | futuristic | artisanal | luxury | technical | experimental
- Secondary vibe label (optional)
- Motion regime label: subtle | kinetic-type | scroll-scene | cursor-led | mixed | minimal-motion
- Materiality label: matte | glossy/chrome | grain/film | clean-digital | textured | mixed
Also produce:
- 3–6 bullet rationale referencing what the model sees (type, spacing, media, motion cues)
- A short “do/don’t” list (2–3 each)

Store in the descriptor JSON under keys:
vibe.primary, vibe.secondary, motion.regime, materiality, rationale[], do[], dont[]

# 5) Taxonomy and clustering (10–15 clusters)
Create:
taxonomy/style_taxonomy.yaml
- definitions for each cluster
- allowed labels and how to use them
- exemplar site_ids (2–4 per cluster)

Also create:
taxonomy/clusters.json
- each cluster: centroid summary (typography, palette behavior, motion regime, media dominance)
- cluster keywords for retrieval

Clustering can be manual for MVP, but must be explicit and consistent.

# 6) Retrieval and synthesis
Given:
- user brief (product, audience, CTA, constraints)
- user references (URLs or corpus IDs; 3–8)
- intensity slider (0–3)
the system must:
- find 8–12 nearest corpus neighbors (by tags/cluster + optional embeddings)
- compute “Shared DNA” summary:
  typography plan tendencies, palette restraint, media dominance, motion tempo/easing, layout grammar
- output a ranked list of “evidence” references (site_ids) used for synthesis

Store retrieval output as:
runs/<run_id>/retrieval.json

# 7) Generation artifacts (required outputs)
For each run, write:

7.1 Direction Pack (runs/<run_id>/DIRECTION.md)
Must include:
- Design thesis (one sentence)
- Mood triad (3 adjectives, define each in context)
- Typography system (2 families max; roles; type scale; line length targets)
- Color strategy (background/foreground/accent logic; contrast rules)
- Layout grammar (grid rules, asymmetry, whitespace policy)
- Media strategy (photo/video/3D: what, where, why; fallback plan)
- Motion grammar (tempo, easing family, transition types, max motion density)
- Signature interaction (exactly one for MVP unless intensity=3; describe behavior)
- Anti-patterns (explicitly forbid 5 common generic landing tropes)

7.2 Motion Storyboard (runs/<run_id>/MOTION.md)
Must include:
- Entry sequence (first 3–5 seconds)
- Scroll beats (0–20–40–60–80–100%) with what changes at each beat
- Section transitions (how they feel, not just “fade”)
- Reduced-motion plan: what becomes static, what remains, how users still understand the narrative
- Performance notes: pinned sections budget, video usage, lazy-loading strategy

7.3 Asset Bible (runs/<run_id>/ASSETS.md)
Must include:
- Shot list: hero + 6–12 supporting assets
- Style recipe: camera/lens, lighting, mood, texture/grain, composition rules
- Prompt blocks for:
  - image generator (hero still + supporting set)
  - video generator (2–4 loops, 3–6s each)
- Consistency rules across generations (palette, lighting continuity, subject continuity)
- Fallback plan: static posters, gradient/noise substitutes if generators unavailable

7.4 Page Plan (runs/<run_id>/PAGE_PLAN.md)
Must include:
- Section narrative (not generic “features/pricing”; use a story arc)
- For each section: goal, content, layout intent, interaction intent, media slot(s), CTA logic
- Responsive intent: what changes on mobile, what stays

7.5 Design Tokens (runs/<run_id>/TOKENS.json)
Include:
- colors: bg/fg/accent + neutrals
- typography: families, sizes, weights, tracking, line heights
- spacing scale
- radii + shadows
- motion: durations + easing names
- z-index scale

# 8) Code scaffold (Next.js + Tailwind + GSAP)
Generate a working scaffold under runs/<run_id>/app/ (or /src/) that includes:
- A single landing page route with 6–10 sections per PAGE_PLAN
- Tailwind config using TOKENS
- GSAP ScrollTrigger hooks implementing MOTION beats (with reduced-motion checks)
- Media components:
  - VideoBackground with lazy load + poster + prefers-reduced-motion fallback
  - ResponsiveImage with srcset guidance
- Accessibility basics:
  - semantic landmarks
  - focus states
  - keyboard navigability
  - alt text placeholders tied to ASSET slots
- Performance basics:
  - avoid layout shift
  - defer non-critical animation init
  - avoid scrolljacking by default (Lenis optional and gated)

The code must run without missing imports and should not depend on obscure libraries.

# 9) Quality gates (must pass before “done”)
Provide a checklist in runs/<run_id>/QA.md and ensure the scaffold meets:
- Reduced motion works (prefers-reduced-motion)
- No horizontal scroll on mobile
- Focus visible on interactive elements
- Images/videos have placeholders and do not block render
- One signature interaction only unless intensity=3
- Typography hierarchy consistent across sections

# 10) Final output for MVP
The MVP is complete when:
- corpus contains 30–50 captured sites with descriptors
- taxonomy has 10–15 clusters with exemplars
- a demo run can be executed from a brief + 3 references and produces:
  DIRECTION.md, MOTION.md, ASSETS.md, PAGE_PLAN.md, TOKENS.json, QA.md, and a runnable Next.js scaffold

Deliver repository structure, scripts/commands to run capture + analysis + generation, and one sample run committed as an example.
