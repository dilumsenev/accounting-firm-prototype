# Ledger & Co. CPA Landing Page - Implementation Plan

This is the numbered checklist of every section that will be built for the single-file (`index.html`) landing page.

1. **Nav**: Sticky navigation bar with logo, phone number, CTA, desktop links, and mobile hamburger menu.
2. **Hero**: Dark Slate Navy header with title, sub-line, dual CTAs, stats row, and subtle decorative background circles.
3. **Social Proof Strip**: White section featuring a 3-column grid of client outcome quotes, with the first highlighted.
4. **Comparison Block**: Distinctive split-card (White vs. Slate Navy) comparing a typical CPA with Ledger & Co.
5. **Problem Section**: White section identifying pain points via a 3-column emoji-led card grid.
6. **Services**: 3-column grid highlighting key offerings (Tax, Bookkeeping, Payroll) with hover interactions.
7. **Pricing Signal**: Dark Slate Navy section displaying three pricing tiers with a highlighted central option.
8. **FAQ**: Single-open accordion containing common questions in a bordered container.
9. **Final CTA**: Minimal contact form for email capture, response promise, and alternative contact links.
10. **Footer**: Simple dark footer with logo, copyright, and policy links.

## Open Questions
- None at this time. The design tokens, typography, and specific copy are very well defined.

## Proposed Changes
### Landing Page Structure
#### [NEW] [index.html](file:///Users/dilumsenev/Documents/Google%20Antigravity/Accounting%20Firm%20-%20Prototype/index.html)
- A single HTML file encompassing all HTML structure, CSS styling, and Vanilla JavaScript functionality.

## Verification Plan
### Manual Verification
- Verify that Google Fonts load correctly and the exact design tokens are applied without deviation.
- Verify responsive stacking of columns on mobile (`min-width: 375px`).
- Verify JavaScript behaviors: sticky nav shadow, mobile nav toggle, service card hover effects, and single-open FAQ accordion functionality.
- Verify that the layout respects the `prefers-reduced-motion: reduce` media query.
