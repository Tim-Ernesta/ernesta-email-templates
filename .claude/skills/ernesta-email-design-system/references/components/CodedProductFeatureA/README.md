Product feature A: complete, responsive email HTML (600px, Outlook-safe), kept verbatim at `email-code/templates/product-feature-a.html`. It is the coded version of the Figma template of the same name; see the ProductFeatureTemplate card for the design.

Structure of the wrapper table, one `<tr>` per module:
1. Header strip (value-props variant)
2. Hero: background photo, wordmark, H1, lead paragraph, button
3. Image row: three photos
4. Steps: H2 header and numbered image/text rows
5. Reviews module, dark: quote, attribution, five-star row
6. Product grid: eyebrow with text link and product tiles
7. SMS banner (required)
8. Footer (required)

Required in every email: row 1 is the header strip and the last two rows are the SMS banner and footer. They come from `email-code/blocks/` and stay verbatim.

How to use it:
- Copy the file, then change only content: copy, links, images, the `<title>` and the hidden preheader text.
- Keep the shared `<style>` block and mobile classes (`m-pad`, `m-h1`, `stack`, `dsk`, `m-show`); the head is identical in all four templates and documented in `email-code/shell.html`.
- Images are referenced as `images/<name>` and are not in the repository (only the HTML is). Host the images and update the paths. The card above shows grey placeholders for that reason.
- Merge tags: `{{ unsubscribe_url }}` in the footer; `#####` is the SMS short code.
- Source repository: https://github.com/Tim-Ernesta/ernesta-email-templates.
