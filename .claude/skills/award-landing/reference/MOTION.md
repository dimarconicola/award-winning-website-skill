# Motion Patterns

Use these pattern names. Implementation is your domain.

| Pattern | What It Does | When to Use |
|---------|--------------|-------------|
| Smooth Scroll | Lerp-based scroll with easing, replaces native scroll | Foundation for premium feel |
| Split Text | Break text into chars/words/lines, animate individually | Kinetic headlines, character-by-character reveals |
| Scroll Pin | Pin element in viewport while scrolling through content inside it | Scroll-driven reveals, Apple-style product sections |
| Parallax Layers | Elements move at different speeds relative to scroll | Depth, multi-speed backgrounds |
| Magnetic Hover | Element follows cursor within radius, snaps back on leave | Cursor-led CTAs, playful buttons |
| Clip-Path Reveal | Animate clip-path from hidden to visible | Dramatic text entrances, wipe effects |
| Image Reveal | Scale from 0 + clip-path, parent overflow hidden | Dramatic image entrances with scale |
| Horizontal Scroll | Vertical scroll drives horizontal container movement | Galleries, case study showcases |
| Infinite Marquee | Seamless looping horizontal scroll, duplicated content | Logo bars, scrolling testimonials |
| Scroll Video | Scrub video frames based on scroll position | Frame-by-frame product reveals |
| Custom Cursor | Replace default cursor with branded element that follows mouse | Signature cursor that reflects brand |
| View Transitions | Shared-element morphing between pages via View Transitions API | Cross-page cinematic transitions |

> Always respect `prefers-reduced-motion`. Replace with instant states.
