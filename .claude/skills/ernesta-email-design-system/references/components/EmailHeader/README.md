Every email opens with exactly one header strip. It is the first row of the 600px wrapper table, before the hero. Copy the block verbatim from `email-code/blocks/` and change only the words.

Three coded variants, all `#262933` ground with `#f8f6f3` Arial text, 8px vertical padding:
- **Promo** (`header-promo.html`): sentence-case promo line, 13px / 500 weight. Used by Back in stock. Placeholder text is "Promo messaging here"; replace it.
- **Tagline** (`header-tagline.html`): uppercase 11px tagline with 0.55px tracking, "DESIGNER QUALITY, CUSTOM-SIZED RUGS". Used by Editorial.
- **Value props** (`header-value-props.html`): uppercase 12px marquee of five claims separated by bullets: Made-to-measure, 2-4 week delivery, Complimentary consultation, Generously sized samples, Premium materials. Used by both Product feature layouts.

Rules:
- Never send an email without a header strip, and never use two.
- Match the strip to the email type: promo for restock and offers, tagline for editorial, value props for launches.
- The Ernesta wordmark is not in the strip; it sits in the hero (`images/logo-light.png`, 105 x 27).
- The hidden preheader text in the `<body>` (the first `div` after `<body>`) is separate; set it for every send.

Figma equivalents: PreHeader (dark, left-split or center) and the Value prop marquee on the Templates page.
