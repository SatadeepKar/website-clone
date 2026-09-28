# Frugal Testing — Landing Page

A single-file landing page (`index.html`) with a working date-picker booking widget, animated live-dashboard hero mockup, real client logos/case studies, and scroll-triggered reveal animations. No build step — open the file directly in a browser.

## Animations

All motion respects `prefers-reduced-motion` (the existing blanket rule near the top of `<style>` disables every `animation`/`transition` for users who ask for reduced motion).

- **Hero** — eyebrow, headline, subhead, copy, CTAs, and stat row fade/slide in on load in sequence (`hu` keyframe, staggered `animation-delay`). The dashboard card follows, then its own contents populate in turn: the progress bar fills 0→78% (`fb` keyframe), the three metric tiles pop in, then the four test rows, then the severity/flow strip.
- **Trust bar** — the client-logo row (`.lg`) is duplicated via JS and scrolls in a seamless infinite marquee (`mq` keyframe); hovering pauses it.
- **Problem section** — the four problem cards, the heading, and the closing pull-quote fade up on scroll with a staggered delay (`.rv`/`.rv.in`, driven by an `IntersectionObserver`). The red/amber highlight inside each card's code snippet pulses gently to draw the eye (`sp` keyframe).
- **Process timeline** — the connecting line draws left-to-right (`scaleX`) as the section scrolls into view, and each of the five step markers pops in with a slight overshoot, staggered in sequence.

The scroll-reveal mechanism reuses the same `IntersectionObserver` pattern already used for the animated stat counters further down the page (`data-n` elements), just generalized to any element carrying the `.rv` class, plus the `.st` timeline container.

## Editing

- Brand colors, spacing, etc. are all CSS custom properties under `:root` (`--yl` is the accent yellow, `--fg`/`--b` the navy, `--c` the cream card background).
- Services (`#sv`) and industries (`#in`) are rendered from the `S` array and the comma-separated industry string near the bottom `<script>` — edit those arrays rather than the HTML.
- The booking widget is a self-built calendar (not Calendly) that hands off to a `mailto:` link with the chosen date/time pre-filled — no external booking service required.

## Worth double-checking before this goes further

This file was uploaded already filled in with real-looking specifics (client logos, case-study links, ISO certifications, a `frugaltestingid.com` contact address) — worth a final sanity pass to confirm every one of those is current and correct, since this session couldn't reach frugaltesting.com to cross-check them directly.
