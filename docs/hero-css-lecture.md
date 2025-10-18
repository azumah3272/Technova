# Hero CSS Lecture — Detailed Explanations

This document explains the CSS rules used for the hero section and the header.
It's written as a teaching resource so you can learn why each rule is written the way it is.

## Global reset

* `* { box-sizing: border-box; margin: 0; padding: 0 }`
  - `box-sizing: border-box` makes width/height include padding and border. This simplifies layout math.
  - `margin: 0; padding: 0` removes browser default spacing so layouts are predictable.

## Body

* `body { font-family: 'Poppins','Roboto',sans-serif; color: #fff; background: linear-gradient(...), url(...) center/cover no-repeat fixed; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale }`
  - Uses system fonts fallback, sets text color to white because the background image is dark.
  - Background uses a subtle dark gradient over an image to improve legibility.
  - Font smoothing improves text rendering across platforms.

## Container

* `.container { max-width: 1200px; margin: 0 auto; padding: 20px }`
  - Centers page content and provides horizontal padding.
  - `max-width` keeps content readable on large screens.

## Header

* `.header-grid { display: grid; grid-template-columns: auto 1fr; align-items: start; gap: 32px; width: 100% }`
  - Two-column grid: logo (auto) + nav (flexible). `gap` controls space between columns.

* `.header-grid figure img { width: clamp(120px, 18vw, 260px); border-radius: 50% }`
  - Makes the logo responsive while keeping it circular.

* `.header-grid nav { justify-self: end; align-self: start; background: rgba(0,0,0,.45); padding: 8px 14px; border-radius: 8px; box-shadow: 0 6px 18px rgba(0,0,0,.28); margin-left: 12px }`
  - Positions the nav to the right and gives it a translucent background for contrast against the logo.

## Hero

* `.hero { display: grid; grid-template-columns: 1fr auto; gap: 20px; margin: 28px 0; align-items: center }`
  - Main layout for the hero: flexible text column + auto image column.

* `.hero h1 { text-align: center; font-size: clamp(28px, 4.2vw, 48px); margin: 40px 0 }`
  - Responsive heading size.

* `.hero-text { display: flex; flex-direction: column; gap: 12px }`
  - Stacks text content vertically with consistent spacing.

* `.hero-image img { width: clamp(180px, 22vw, 360px); padding: 12px; background: rgba(0,0,0,.35); border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,.35); object-fit: cover }`
  - Image is a card with padding/background/shadow for separation from the page background.

## Responsive behavior

* Media queries collapse grid to a single column under 900px/840px/640px where appropriate. This ensures the layout reads well on tablets and phones.

## Notes and tips

- Use DevTools to experiment: change `clamp()` values and `gap` to see live effects.
- Accessibility: ensure color contrast—use `a:focus` styles and provide skip links for keyboard users.

If you'd like, I can extend this lecture with small exercises and screenshots showing before/after.