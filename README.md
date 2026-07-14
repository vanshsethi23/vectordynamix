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

- Social links point at the live `vectordynamixai` handles on LinkedIn, Instagram, YouTube, and X.
- The "Book a Discovery Sprint" CTA opens `mailto:founder@vectordynamix.com`. Swap in a scheduling link (Calendly etc.) when available.
- The "Send us a message" form delivers submissions to founder@vectordynamix.com via Web3Forms (no backend), submitting over AJAX so the visitor stays on the page and sees an inline success or error message. Set the access key: get a free one at https://web3forms.com (enter founder@vectordynamix.com, the key arrives by email) and paste it into `WEB3FORMS_KEY` in the message-form script in `index.html`. Until a key is set, Send opens the visitor's mail client pre-filled (no errors). Includes a spam honeypot.
- The newsletter form still hands off to email (mailto). Wire it to an email service provider before launch.
