# Visual Optimization Plan

This document outlines an actionable, step-by-step plan to implement the visual design suggestions for the Ledger & Co. CPA prototype (`index.html`). 

## Phase 1: Imagery & Asset Upgrades
- [x] **Task 1.1: Replace Emojis with SVGs.** In the Problem Section, replace text emojis with custom SVG icons (e.g., Lucide or Feather Icons) for a cleaner, professional look.
- [x] **Task 1.2: Add Testimonial Headshots.** Insert high-quality, circular client headshots in the Social Proof section to humanize the quotes and build trust.
- [ ] **Task 1.3: Enhance Hero Visuals.** Add a subtle dashboard mock-up, abstract graphic, or lifestyle image to the right side of the Hero section for desktop layouts.
- [x] **Task 1.4: Update List Icons.** Swap the standard text symbols (X and Checkmarks) in the Comparison Block and Pricing sections with polished SVG icons for sharper rendering.

## Phase 2: Micro-Interactions & Animations
- [x] **Task 2.1: Scroll-Triggered Reveals.** Implement an intersection observer (using vanilla JS) to subtly fade in and slide up elements (Hero text, Service cards, Problem cards) as they scroll into view.
- [x] **Task 2.2: Dynamic Backgrounds.** Add a slow, infinite CSS `@keyframes` rotation animation to the `.hero-bg-circles` to make the section feel alive.
- [x] **Task 2.3: Refine Card Hover States.** Enhance the hover effects for `.service-card` and `.price-card` by adding a slight scale transform (`transform: scale(1.02)`) and a softer, larger drop-shadow.
- [x] **Task 2.4: Button Animations.** Add a subtle glow or fill-sweep hover animation to the primary buttons.
- [x] **Task 2.5: Nav Glassmorphism.** Apply a frosted glass effect (`backdrop-filter: blur(12px)`) with a slightly transparent background to the sticky navigation bar instead of a solid white background.

## Phase 3: Color, Texture & Typography Polish
- [x] **Task 3.1: Subtle Gradients.** Introduce a very faint, deep radial gradient (or mesh gradient) to the background of the dark Hero and Pricing sections to add depth.
- [x] **Task 3.2: Texture Overlays.** Apply a subtle CSS noise texture overlay to the dark sections (Hero, Pricing, Footer) for a premium, tactile "print-like" aesthetic.
- [x] **Task 3.3: Typography Contrast.** Increase the contrast in font weights between headers and body text.
- [x] **Task 3.4: Mobile Readability.** Fine-tune line heights and font sizes on mobile devices to optimize readability.

## Phase 4: Layout & UX Refinements
- [x] **Task 4.1: Mobile Sticky CTA.** Add a floating, sticky "Book a Call" button fixed to the bottom of the screen on mobile devices so the primary conversion action is always accessible.
- [x] **Task 4.2: Service Card Staggering.** Stagger the layout of the three Service cards (e.g., pushing the center card slightly downward) to create a dynamic, slightly asymmetrical layout that breaks the rigid grid.
