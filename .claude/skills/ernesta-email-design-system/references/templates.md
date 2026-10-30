# Templates and live emails

Open the **Templates** and **Emails** groups on the Components tab to see each design rendered from Figma.

## Starting points (Templates page in Figma)
- **Back in stock**: PreHeader, Hero, ProductGrid, ReviewsModule, SupportBar, PreHeader (SMS), Footer. See `BackInStockTemplate`.
- **Product feature**: Value prop marquee, Hero, then layout A (ImageGridModule, ImageTextStepsModule, ReviewsModule, ProductGrid) or layout B (ProductFeature, Ctas, ImageTextStepsModule, SupportBar). See `ProductFeatureTemplate`.
- **Editorial**: PreHeader, Hero, then layout A (SingleColumn, ImageCollage, three-column product grid, three-column feature cards) or layout B (ImageImageModule, three-column product grid). See `EditorialTemplate`.

Each exists at 600px desktop and 390px mobile; use the same modules in the same order on both.

## Coded templates (GitHub: Tim-Ernesta/ernesta-email-templates)
Production-ready, responsive HTML for four of the layouts, kept verbatim under `email-code/templates/`:
- `back-in-stock.html`, `editorial.html`, `product-feature-a.html`, `product-feature-b.html` (components `CodedBackInStock`, `CodedEditorial`, `CodedProductFeatureA`, `CodedProductFeatureB`).
- They share one `<head>` and mobile stylesheet (`email-code/shell.html`), one SMS banner and one footer. Only the header strip differs: promo (Back in stock), tagline (Editorial), value props (Product feature).
- **Every email gets a header strip first, the SMS banner and the footer last.** See `EmailHeader`, `SmsBanner`, `EmailFooter`.
- The Editorial desktop B layout, the mobile layouts and the lifecycle emails have no coded version yet; build them from the closest coded template and the Figma renders.

## Live lifecycle emails (Current designs page in Figma)
- `WelcomeEmail` (three versions), `PersianEditEmail`, `CustomSizing101Email`, `SampleEmail`, `RoomvoEmail`.
- Reusable patterns across them: a dynamic "Pick up where you left off" row with an `[STYLE]` merge field, "Collections to explore" four-row image stack, "Experience for yourself" photo with two outline buttons, an Instagram strip, and the standard Footer.

## Every send ends with
PreHeader (SMS prompt), SupportBar (or the Value prop marquee at the top for Product feature), Footer with Unsubscribe.

## How to choose
- One product or restock: Back in stock.
- Launch or collection explainer: Product feature.
- Story, process or education: Editorial, or copy a lifecycle email that is closest.
- When a lifecycle email already covers the pattern (sizing guide, sample box, visualizer), reuse its module order.
