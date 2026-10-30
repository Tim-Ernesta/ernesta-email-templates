Build every Ernesta newsletter from the modules in `components/`, stacked in the order given in `templates.md`. Start from the closest template or live email (Templates and Emails groups), then swap modules using the Atoms, Molecules and Modules groups; `figma-file.md` maps every Figma page to its place here. Emails are 600px wide on desktop and 390px on mobile; write table-based HTML with inline styles and a 24px (`space-4`) side gutter.

## Required in every email
Every email, whatever the template, has the same frame. Copy these blocks verbatim from `email-code/blocks/` and change nothing but content:
1. **Header strip first** (`EmailHeader`): exactly one of the promo, tagline or value-props strips, `#262933` with `#f8f6f3` text, above the hero.
2. **SMS banner** (`SmsBanner`) directly above the footer.
3. **Footer last** (`EmailFooter`), unchanged, with the working Unsubscribe link (`{{ unsubscribe_url }}`).
The `<head>`, mobile styles and wrapper table are shared too (`email-code/shell.html`). Complete coded examples are in `email-code/templates/` (Coded templates group): back-in-stock, editorial, product-feature-a, product-feature-b. Start every new email from one of them or from the shell.

## Content fundamentals
- Headlines are short, sentence-style and in serif: "Back in Stock". Eyebrows, subheaders and buttons are UPPERCASE sans.
- Write to the customer ("Reach out to our design team"), never "we are pleased to announce". No emoji.
- One primary action per module. Button labels are one to three words: "Shop now", "Order a sample box".
- Product blocks follow Name, one-line romance description, then an underlined text link.
- Never hardcode placeholder copy such as "Lorem ipsum" or "Promo messaging here" into a send.

## Visual foundations
- Ground is cream `surface` (#f8f6f3) with `ink` (#262933) text. Dark modules (pre-header, dark Reviews, Footer, buttons) use `ink` with `on-ink` text. Support banner uses `banner-mist` with `ink` text.
- Headlines use the serif `h1`–`h4`; everything else uses the sans styles `eyebrow`, `body-large`, `body-regular`, `body-small`, `text-links`, `button`. Letter-spacing is -1% on headlines and body, +5% on eyebrows and buttons.
- Buttons: `ink` fill, `on-ink` label in the `button` style, `radius-xs`, padding 16px 32px (`space-3` / `space-5`).
- Photography is full-bleed, warm and interior-led (rugs in room settings); product tiles use a square `surface-white` ground with the rug cropped to the tile.
- Dividers: a 1px dotted rule in `on-ink` on dark modules, a 1px solid hairline (`ink` at 20%) on light ones. No shadows, no gradients.
- Mobile uses the smaller type sizes noted on each style and stacks two- and three-column rows into one column.

## Patterns from the live emails
- Buttons on cream or white photography are often the outline style (1px `ink` border, `ink` label); over dark photography use a solid white button with `ink` label. Solid `ink` buttons appear on cream and linen grounds.
- "Pick up where you left off" is a dynamic row with a `[STYLE]` merge field in its button; keep the bracketed token exactly as written until the ESP replaces it.
- Section titles inside lifecycle emails are sentence-case serif ("Our sizing philosophies", "Experience for yourself"); small caps eyebrow labels ("ABOUT ERNESTA", "COLLECTIONS TO EXPLORE") introduce grouped content.
- A hero may take a one-off ground color for a collection (the Persian Edit is deep blue); everything below it returns to cream and ink.
- Inline links in body copy are underlined `ink`; a mockup or illustration disclaimer sits under the image in 10px caps.

## Email engineering rules
- Tables only for layout, `role="presentation"`, inline styles. Put a `<style>` media query (`max-width:480px`) in the head for stacking and the mobile type sizes.
- Fonts: Portonovo and Reader Pro are brand faces that are not web-safe in email. Always send the fallback stacks in `tokens.json` (`font-serif`, `font-sans`) and expect Georgia and Helvetica in most clients.
- Hero images are `<img>` with explicit `width`, `height` and alt text; overlay text uses a background image with a VML fallback for Outlook, or stacks text under the image when VML is not available.
- Every image needs alt text; every link text must make sense without the image.
- Keep the pre-header, support bar and footer in every send; the footer carries the unsubscribe link.

## Assets
The `references/renders/` folder holds Figma renders of every template, live email, atom, molecule and module, for reference. They are screenshots, not production images. The Ernesta script wordmark and the social icons are part of the Figma library and are not exported as standalone files here; export the wordmark from Figma and host it, or set "Ernesta" in the serif style until it is available.
