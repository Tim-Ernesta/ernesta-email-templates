# Figma file map

Source: Ernesta Email Component Library, file key `dAMxIWTCyv3Hk8nALva1GM` (https://www.figma.com/design/dAMxIWTCyv3Hk8nALva1GM/Ernesta-Email-Component-Library). Everything in this system comes from these pages.

| Figma page | Node | What it holds | Where it is here |
| --- | --- | --- | --- |
| Getting Started | `3007:2113` | Empty | none |
| Cover | `1:20` | Library cover ("Email Component Library") | `TypeSpecimen` card |
| Templates | `3005:2022` | Three templates, desktop and mobile | Templates group |
| Examples | `3064:13776` | The same three templates filled with real photography | Not duplicated; use the Templates renders |
| Reference > Current designs | `1:32` | Live lifecycle emails | Emails group |
| Reference > Inspo | `1:34` | Empty | none |
| Components > Atoms (locked) | `1:11` | 8 atoms | Atoms group |
| Components > Molecules | `3007:2125` | 21 molecule component sets | Molecules group |
| Components > Modules | `3056:7953` | 20 module component sets | Modules group |
| Style Guide | `54:12` | Desktop and mobile type specimens | `tokens.json`, `TypeSpecimen` |
| Archive | `14:2` | Empty | none |

## Variables and styles in the file
- One variable collection, **Type**, with modes `large` and `small`: families (serif Portonovo, sans Reader Pro), sizes and weights for h1 to h4, body-large, body-regular, body-small, text-links and buttons.
- Nine text styles: H1-serif, H2-serif, H3-serif-regular, H4-serif, H4-eyebrow, body-large, body-regular, text-links, button.
- There are no color variables or paint styles. The colors in `tokens.json` were read from the fills used across the three templates (#f8f6f3, #262933, #ffffff, #f6f4f1, #c8cdd0).
- There are no effect styles. Emails use no shadows.

## Refreshing this system from Figma
Re-export the renders with the Figma MCP (`get_screenshot` by node id above), replace the files under `references/renders/`, and re-read `tokens.json` values from the Type collection. Component names differ from Figma in these cases: `hero-modules` is Hero, `product-grid-module` is ProductGrid, `two-column-image-image-text` is ImageText, `Email Footer-Updated` is Footer, `CTA's` is Ctas (molecule) and CtaButtons (atom), `Divider` atom is DividerAtom.
