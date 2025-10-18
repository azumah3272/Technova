# Projects Section — Design & CSS Lecture

This lecture explains the changes made to the Projects section and why they help your portfolio convert visitors into leads.

## Goals for the Projects section
- Use marketable language that communicates value quickly.
- Present projects as clickable cards with an image, title, and short benefit-driven sentence.
- Keep layout consistent with site (dark, slightly translucent cards, soft shadows).
- Make the grid responsive: cards reflow depending on screen width.

## HTML structure recap
- `section.projects-section` — wrapper for the entire area.
- `header.projects-header` — heading + lead paragraph.
- `div.projects-grid` — CSS grid container for cards.
- `article.project-card > a.card-link` — clickable card that contains the image and content.

This semantic structure helps accessibility and SEO: headings remain clear, articles are content blocks, and links wrap the whole card for an easy tap target on mobile.

## CSS rules (explained)
- `.projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 22px }`
  - `repeat(auto-fit, minmax(...))` builds a responsive grid that fits as many columns as possible; each card is at least 240px wide and expands to fill available space.
  - `gap` controls the space between cards. Adjust if you want denser or airier layouts.

- `.project-card { background: linear-gradient(...); border-radius: 12px; overflow: hidden; box-shadow: ...; transition: transform .18s ease }`
  - The translucent gradient keeps the card subtle on top of the page background while ensuring text remains readable.
  - `overflow: hidden` prevents child elements (like images) from escaping rounded corners.
  - `transition` + `:hover` lift provides a tactile feel and encourages clicks.

- `.project-card img { width:100%; height:160px; object-fit:cover }`
  - Fixed-height previews keep the grid aligned and consistent. `object-fit: cover` crops the image while preserving aspect ratio.

- `.project-card .card-content { padding: 14px }`
  - Consistent spacing between the image and text.

- `.project-card h3` and `p`
  - Heading is the project name. The paragraph is benefit-oriented copy (not a feature list).

- `.project-card:hover { transform: translateY(-6px); box-shadow: ... }`
  - Micro-interaction that signals clickability and draws attention without being noisy.

## Accessibility notes
- Ensure alt attributes describe what users will see.
- Wrapping the whole card in an anchor makes the tap target larger and better for mobile users.
- Make sure contrast remains acceptable on all cards. If images are bright or busy, consider an overlay or stronger background behind text.

## How to tune for conversions
- Use verbs in headings (Preview, Explore, Try) and benefit statements (e.g., "Increase engagement by 30% with accessible design").
- Add small badges ("Featured", "Demo") if you have time-sensitive or noteworthy projects.
- Track clicks on cards (event tracking) to see which case studies generate interest.

## Next exercises
1. Add a small tag/badge to each card (e.g., <span class="badge">Featured</span>) and style it.
2. Replace the static height image with a background-image on `.project-card` and overlay title text for a dramatic hero card.
3. Add keyboard focus styles for `.card-link` so that keyboard users can see focus when tabbing.

If you want, I can implement exercise 1 now (badges) and show the code and explanation.