Plan: UI fixes for hero, testimonials, portraits, and chat widget

Problem statement

- Navbar buttons become excessively rounded and clip the hero on mobile.
- Two supporting snippets next to the 100+ five-star reviews read "Trusted by clients in 27+ states" and "Registered in all 50 states". For a small firm these feel off and conflict with the statistics below.
- Second testimonial shows a single letter for the portrait (looks like a fallback avatar); confirm intent.
- Add a generic portrait image for Sarah Mitchell.
- Chat widget: add a dotted handle (desktop only) to allow dragging; clicking the bubble currently does nothing — provide a hardcoded open/close and a simple welcome message in the widget.

Approach summary

- Make small, targeted CSS/markup changes. Mobile navbar: reduce border-radius on buttons and add responsive layout rules to prevent clipping the hero (overflow/position fixes).
- Replace the two trust snippets with firm-appropriate short items (suggestions included). Update copy and aria labels.
- Verify testimonials data source; if avatar is intentionally a letter fallback, provide design guidance. If not, use provided portrait images or add generic fallback avatars.
- Add a generic portrait image asset for Sarah Mitchell and wire it into the team member card.
- Implement a lightweight chat widget behavior: a draggable bubble (desktop-only) with a dotted drag handle; onClick toggles a small chat panel with a hardcoded welcome message and a close button. Keep implementation JS/CSS-only (no external chat provider), gated to desktop widths.

Files / areas to change (likely)

- src/components/Header.\* (or header.html / header.scss)
  - adjust button border-radius in mobile media queries; ensure positioning/overflow don't overlap hero
- src/styles/\_buttons.scss or global CSS variables
  - define responsive border-radius and spacing tokens
- src/components/Hero.\* (or hero.scss)
  - ensure top padding accounts for header height at mobile widths; add z-index/overflow rules
- src/components/TrustBar.\* (the line with stars and snippets)
  - replace copy for the two snippets and adjust separators and responsive wrapping
- src/data/testimonials.\* or content/testimonials.json
  - confirm avatar fields; update second testimonial data if needed
- src/components/TeamMember.\* (Sarah Mitchell card) and assets/images/
  - add generic portrait image and reference it
- src/components/ChatBubble._ and src/components/ChatPanel._
  - implement draggable handle (desktop-only), click toggle, basic welcome message markup and styles
- src/js/main.js or equivalent global script
  - small JS to wire drag + toggle behavior; guard by matchMedia for desktop

Suggested copy replacements for the two snippets (examples)

- Replace "Trusted by clients in 27+ states" with: "Serving clients across multiple states"
- Replace "Registered in all 50 states" with: "Registered where clients need us" or "Licensed in key states" (pick tone that fits firm)

Design notes / constraints

- Keep visual rhythm with existing typography and separators. Avoid adding heavy iconography beside the stats.
- Chat bubble draggable handle: small dotted 3x3 vertical dots to the right of the bubble; only visible on min-width: 1024px.
- Clicking the bubble opens a panel anchored to the bubble's position (simple absolute positioning).
- Provide ARIA attributes for toggles and buttons (aria-expanded, aria-label).

Verification steps

1. Resize to mobile widths (~375–420px): header buttons maintain modest radius and no overlap with the hero headline; hero top padding remains visible.
2. Trust snippets updated and wrap gracefully on small screens.
3. Testimonials: second testimonial shows either photo or consistent fallback avatar (not a single-letter unless intended).
4. Sarah Mitchell card uses new generic portrait asset.
5. Chat bubble: on desktop, dotted handle visible; dragging moves bubble within viewport; clicking toggles panel showing hardcoded welcome message and close button. On mobile, bubble stays fixed and click does not open (or optionally opens full-screen — choose later).

Todos (tracked separately)

- navbar-mobile-fix: Fix header button radius and clipping at mobile widths
- trust-snippets-replace: Replace the two snippets next to review stars with firm-appropriate copy
- testimonial-avatar-check: Confirm intent for single-letter avatar and fix fallback
- add-sarah-portrait: Add a generic portrait for Sarah Mitchell and wire into her card
- chat-widget-drag-and-open: Implement draggable dotted handle (desktop) and hardcoded open/close behavior

Notes for implementation order and risk

- Start with CSS for navbar and hero spacing (low risk). Verify across breakpoints.
- Update copy/snippets next (content change, low risk).
- Portrait and testimonial fixes are content or data changes — quick but verify sources.
- Chat widget requires small JS; keep scoped and guarded by desktop-only checks. Test drag behavior and keyboard accessibility.

If anything unclear: ask which copy variant to use for the two snippets and whether clicking the chat bubble should also be available on mobile (current request asked desktop-only for dragging; leave open for mobile behavior).
