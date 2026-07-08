# VectorDynamix — Motion Site

Scroll-driven marketing site for VectorDynamix, the AI Operating Systems Partner.

## What's here

- `index.html` — the complete single-file site (all CSS and JS inline)
- `assets/frames/` — 120 WebP frames extracted from the brand video, in desktop (1280x720) and mobile (960x540) resolutions, driven by the scroll-linked canvas in the hero
- `assets/fonts/` — self-hosted DM Sans variable font
- `assets/logo-frames/` — 96 WebP frames from the animated logo lockup, scrubbed by scroll in the outro section before the footer
- `assets/vdx-mark-*.png`, `assets/vdx-wordmark-*.png` — transparent logo assets (dark and light variants)
- `assets/avatars/` — illustrated persona avatars (generated with DiceBear, seeded per person) used in the testimonials carousel
- `assets/service/` — per-service animated mockup videos (`discovery`, `agentic`, `enablement`) with poster frames, shown in the Services cards and autoplayed only while on screen

## Run locally

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

Serve over HTTP (don't open the file directly) so the frame images load.

## Structure

Single page: Home (scroll film: headline plus three story cards) → Services (sticky-stack cards) → Our Approach (timeline) → Why VectorDynamix (bento + comparison) → Testimonials (auto-scrolling carousel) → FAQs → Newsletter → Contact → Outro (scroll-driven logo build) → Footer (message form, email, social links).

## Notes for launch

- Social links point at `/vectordynamix` handles on LinkedIn, Instagram, YouTube, and X. Update if the real handles differ.
- The "Book a Discovery Sprint" CTA opens `mailto:founder@vectordynamix.com`. Swap in a scheduling link (Calendly etc.) when available.
- The newsletter and message forms hand off to email. Wire them to an email service provider or form backend before launch.
