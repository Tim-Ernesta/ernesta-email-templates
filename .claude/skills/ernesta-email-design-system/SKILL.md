---
name: ernesta-email-design-system
description: Ernesta's email design system built from the Ernesta Email Component Library in Figma: tokens, all atoms/molecules/modules, the three newsletter templates and the live lifecycle emails (Welcome, Persian Edit, Custom-sizing 101, Sample, Roomvo). Use whenever building, editing or reviewing an Ernesta newsletter or lifecycle email, choosing email colors, fonts or modules, or when the user mentions Ernesta email components, templates, hero, product grid, reviews module, support bar or footer.
---

# Ernesta email design system

Everything needed is in this skill's `references/` folder. Source: the Figma file "Ernesta Email Component Library" (fileKey dAMxIWTCyv3Hk8nALva1GM, https://www.figma.com/design/dAMxIWTCyv3Hk8nALva1GM/Ernesta-Email-Component-Library). A browsable version lives in the Design System artifact https://claude.ai/artifact/GajxHxzdVqsq9FEaBchaqV (private to its owner unless shared).

## Required in every email
Every email has the same frame; copy these blocks verbatim from `references/email-code/blocks/` and change only content:
1. Exactly one header strip first: `header-promo.html`, `header-tagline.html` or `header-value-props.html` (promo for restock/offers, tagline for editorial, value props for launches).
2. `sms-banner.html` directly above the footer (replace the `#####` short code).
3. `footer.html` last, unchanged, with the Unsubscribe link (`{{ unsubscribe_url }}`).
Start every email from a complete coded template in `references/email-code/templates/` (back-in-stock, editorial, product-feature-a, product-feature-b) or from `references/email-code/shell.html` (shared head, mobile styles, wrapper). Images are referenced as `images/<name>` and are not bundled; host them and update the paths. Source: https://github.com/Tim-Ernesta/ernesta-email-templates.

## Steps
1. Read `references/README.md` (usage rules) and `references/tokens.json` (exact colors, type, spacing, radii).
2. Read `references/templates.md` to pick the closest starting point: Back in stock, Product feature (layouts A/B), Editorial (layouts A/B), or a live email (Welcome, Persian Edit, Custom-sizing 101, Sample, Roomvo). Look at the render:
   - templates: `references/renders/Templates/*.jpg`
   - live emails: `references/renders/Emails/*.jpg`
3. For each module, read `references/components/<Name>/README.md` (variants, toggles, composition, where used) and look at its render in `references/renders/<Atoms|Molecules|Modules>/<figma-name>.jpg` (the README names the file). View the image to see every variant.
4. Coded markup: `references/email-code/` (templates, header, SMS banner, footer, reviews, support bar) and `references/components/<Name>/email.html` for Hero, ProductGrid, FeatureText, ImageText and Ctas. Copy it and swap the content. For the rest, build table-based HTML from the render and the tokens.
5. `references/figma-file.md` maps every Figma page and node id. If a render looks out of date or something is missing, read the node with the Figma tools.
6. Use the `newsletter-recommended-styles` skill for the "Recommended for you" block and review quotes.

## Rules to keep in mind
- Colors: surface #f8f6f3, ink #262933, white #ffffff, linen #f6f4f1, banner-mist #c8cdd0. Dark modules are ink with cream (#f8f6f3) text.
- Fonts: serif headlines (Portonovo, fallback Georgia), sans text (Reader Pro, fallback Helvetica/Arial). H1 48, H2 32, H3 24, H4 18, 600 weight, -1% tracking; body 13-15; buttons 11 uppercase, +5% tracking. Mobile sizes are smaller (H1 32, H2 24, H3 20, H4 16).
- Buttons: solid ink or outline; one primary CTA per module; over dark photography use a solid white button.
- 600px desktop, 390px mobile, table-based HTML with inline styles, 24px side gutter.
- Every send has a pre-header, a support bar (or the value-prop marquee at the top) and the footer with an unsubscribe link.
- Keep `[STYLE]` merge fields in place; keep placeholders such as "Lorem ipsum" out of anything actually sent.
- The renders are Figma screenshots for reference, not production images. The Ernesta wordmark and social icons are not bundled; export them from Figma.
