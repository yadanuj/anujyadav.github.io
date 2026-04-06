# Portfolio Design System: The Digital Architect

This design system is a bespoke framework crafted for a high-end B.Tech IT portfolio. It moves beyond the generic "tech" template, opting instead for a sophisticated, editorial approach that balances academic rigor with forward-thinking innovation.

## 1. Overview & Creative North Star

**Creative North Star: The Precision Academic**
The visual language is defined by "Precision Editorial." It treats code and technical projects as high-art, utilizing expansive white space, intentional asymmetry, and a sophisticated monochromatic-adjacent palette. We break the rigid grid by allowing typography to bleed across sections and using overlapping elements to create a sense of architectural depth. This isn't just a resume; it is a curated exhibition of technical prowess.

---

## 2. Colors: Depth Through Tonality

The palette is anchored in deep teals (`primary: #004d60`) and crisp, airy surfaces. We avoid the "flat" look by utilizing the full spectrum of Material surface containers to create a physical sense of hierarchy.

### The "No-Line" Rule
**Prohibit 1px solid borders for sectioning.** Structural boundaries must be defined solely through background color shifts. For instance, a section utilizing `surface-container-low` should transition directly into a `surface` or `surface-bright` section. This creates a seamless, high-end editorial feel rather than a "boxed-in" web feel.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, premium materials:
*   **Base Layer:** `surface` (#f7fafc) for the primary background.
*   **Interactive Cards:** `surface-container-lowest` (#ffffff) to provide a subtle "lift" against the background.
*   **Nested Elements:** Use `surface-container-high` (#e6e8ea) for inset elements like code snippets or metadata chips within a card.

### The "Glass & Gradient" Rule
To elevate the "forward-looking" tech aesthetic:
*   **Glassmorphism:** Navigation bars and floating action menus should use `surface` at 70% opacity with a `backdrop-filter: blur(20px)`.
*   **Signature Textures:** Use a subtle linear gradient from `primary` (#004d60) to `primary-container` (#00677f) for primary CTAs and hero section accents to inject "soul" into the digital interface.

---

## 3. Typography: The Editorial Scale

We pair **Space Grotesk** (a high-character, geometric sans-serif) with **Inter** (the gold standard for legibility).

*   **Display (Space Grotesk):** Large, assertive, and slightly tracked-in (-2%). Used for Hero headers and major section numbers to create an academic-journal vibe.
*   **Headlines (Space Grotesk):** Medium weight. Used to introduce project titles.
*   **Body (Inter):** Regular weight with generous line-height (1.6). This ensures that even complex technical explanations remain approachable and "clean."
*   **Labels (Inter):** Uppercase with increased letter-spacing (+5%) for metadata like "TECH STACK" or "DATE," providing a technical, "blueprint" feel.

---

## 4. Elevation & Depth: Tonal Layering

Traditional drop shadows are largely discarded in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking" the `surface-container` tiers. A `surface-container-lowest` card sitting on a `surface-container-low` section creates a soft, natural lift without the "muddy" look of standard shadows.
*   **Ambient Shadows:** If a floating element (like a modal) requires a shadow, use a large blur (32px+) at 4%–8% opacity using a tint of `on-surface` (#181c1e).
*   **The Ghost Border:** If a container requires further definition (e.g., in high-density data areas), use the `outline-variant` token at **15% opacity**. Never use 100% opaque borders.

---

## 5. Components

### Buttons
*   **Primary:** Background: `primary` gradient; Text: `on-primary` (#ffffff); Corner Radius: `md` (0.375rem).
*   **Secondary:** Background: `secondary-container`; Text: `on-secondary-container`. No border.
*   **Tertiary:** Ghost style; Text: `primary`. High-contrast interaction on hover (slight `surface-variant` background).

### Cards & Projects
*   **Rule:** Forbid divider lines. Separate project details using vertical white space and font-weight shifts.
*   **Style:** Use `surface-container-lowest` with a "Ghost Border" and `xl` (0.75rem) rounded corners for a modern, friendly tech aesthetic.

### Chips (Tech Stack & Skills)
*   **Action Chips:** Utilize `tertiary-container` (#875219) for specific highlights (e.g., "Award Winning") to provide a warm, "academic gold" accent against the cool blues.
*   **Filter Chips:** Use `secondary-fixed-dim` with `on-secondary-fixed-variant` for a muted, professional look.

### Input Fields
*   **Visual Style:** Subtle `surface-container-highest` background with a bottom-only `primary` focus line (2px). This mimics a "fill-in-the-blank" academic form rather than a generic box.

### Project Timeline (Custom Component)
Instead of a vertical line, use a series of `surface-dim` dots connected by a `surface-variant` background shift. This keeps the layout airy and avoids unnecessary "ink" on the screen.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts (e.g., 60/40 splits) to create visual interest in project case studies.
*   **Do** lean into the "Teal/Blue" palette by using `primary-fixed` (#b6eaff) for large background decorative elements.
*   **Do** use `display-lg` typography for single-word impacts (e.g., "INNOVATION," "LOGIC").

### Don't:
*   **Don't** use pure black (#000000). Use `on-background` (#181c1e) for text to maintain a premium, softened contrast.
*   **Don't** use standard "box-shadows" on every card. Trust the tonal shifts between `surface` tiers to define the space.
*   **Don't** cram content. If a section feels "busy," increase the padding using the top end of your spacing scale. Academic prestige is found in the space between the thoughts.