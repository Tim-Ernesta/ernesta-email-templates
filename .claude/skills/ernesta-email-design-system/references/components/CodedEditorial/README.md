Editorial: complete, responsive email HTML (600px, Outlook-safe), kept verbatim at `email-code/templates/editorial.html`. It is the coded version of the Figma template of the same name; see the EditorialTemplate card for the design.

Structure of the wrapper table, one `<tr>` per module:
1. Header strip (tagline variant): "DESIGNER QUALITY, CUSTOM-SIZED RUGS"
2. Hero: background photo, wordmark, H1, lead paragraph, button
3. Editorial block: H2, H3, body copy and image rows
4. Product grid: H2 header with text link and three-up tiles
5. CTA: "Shop collection" button
6. Support bar: three value props on white
7. SMS banner (required)
8. Footer (required)

Required in every email: row 1 is the header strip and the last two rows are the SMS banner and footer. They come from `email-code/blocks/` and stay verbatim.

How to use it:
- Copy the file, then change only content: copy, links, images, the `<title>` and the hidden preheader text.
- Keep the shared `<style>` block and mobile classes (`m-pad`, `m-h1`, `stack`, `dsk`, `m-show`); the head is identical in all four templates and documented in `email-code/shell.html`.
- Images are referenced as `images/<name>` and are not in the repository (only the HTML is). Host the images and update the paths. The card above shows grey placeholders for that reason.
- Merge tags: `{{ unsubscribe_url }}` in the footer; `#####` is the SMS short code.
- Source repository: https://github.com/Tim-Ernesta/ernesta-email-templates.
