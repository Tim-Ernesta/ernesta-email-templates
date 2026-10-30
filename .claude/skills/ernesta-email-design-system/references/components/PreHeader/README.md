One-line promo or SMS strip, top and bottom of every email.

Figma: Molecules page, node `3017:713` (https://www.figma.com/design/dAMxIWTCyv3Hk8nALva1GM/Ernesta-Email-Component-Library?node-id=3017-713). Layer: Molecule.

Variants (Figma properties):

- **Mode**: light, dark
- **Alignment**: left-split, center

Toggles: Show text link, Show icon, Link swap slot.

Used in: every template (top and above the footer).

HTML preview in this system.

Rendered reference: `references/renders/Molecules/pre-header.jpg` (every variant, exported from Figma). Build the email HTML from that render and the tokens; apply the README rules for type, color and spacing.

**Coded version:** the HTML in this card is the verbatim header strips from the coded templates (`email-code/blocks/header-*.html`). Exactly one header strip is required at the top of every email; see EmailHeader. The SMS banner variant is the SmsBanner component.
