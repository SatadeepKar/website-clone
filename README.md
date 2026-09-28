# Frugal Testing — Landing Page

A single-file, ads-ready landing page (`index.html`) designed to convert paid-traffic visitors into booked QA consultations. No build step — open the file directly in a browser.

## Design approach

- **One primary conversion goal**: every section pushes toward the Calendly booking widget at the bottom (message match for ad campaigns — keep ad copy and hero headline aligned).
- **Above-the-fold clarity**: value proposition, proof stats, and a CTA are visible without scrolling.
- **Low friction**: no signup forms or gated content — booking a call is one click away.
- **Lightweight by design**: no JS framework, no icon library dependency (icons are inline SVG), FAQ accordion and mobile nav use native HTML/CSS (`<details>` + checkbox toggle) instead of JavaScript.
- **Social proof**: stats bar, testimonials, and industry chips build trust before the ask.

## Before publishing — replace these placeholders

Network access to frugaltesting.com and forbes.com was blocked in the session that built this page, so the following were written from general knowledge of the industry/company and **must be verified or swapped**:

| Placeholder | Location | Replace with |
|---|---|---|
| Calendly link | `data-url="https://calendly.com/frugaltesting/free-qa-consultation"` | Your real Calendly event URL |
| Contact email | `hello@frugaltesting.com` (footer + fallback text) | Your real inbox |
| Stats (`40–60%`, `<48 hrs`, etc.) | Hero card | Verified company metrics |
| Testimonials | "Client Feedback" section | Real, approved client quotes |
| Services list | `#services` | Confirm against your current service catalog |
| Logo mark ("FT") | Header/footer | Swap for your actual logo asset if available |

## Customizing

All styling is in a single `<style>` block at the top of `index.html` using CSS custom properties (`--teal`, `--navy`, etc.) — change brand colors in one place under `:root`.
