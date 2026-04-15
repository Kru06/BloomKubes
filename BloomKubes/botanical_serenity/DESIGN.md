# Design System Specification: Editorial Horticulture

## 1. Overview & Creative North Star: "The Living Archive"
This design system is built to evoke the tactile, deliberate pace of a luxury horticultural journal. The Creative North Star is **"The Living Archive"**—an aesthetic that balances the archival permanence of a botanical library with the breathing, organic movement of a greenhouse.

To move beyond the "template" look, this system rejects the rigid constraints of a 12-column grid in favor of **Intentional Asymmetry**. Elements should feel "planted" rather than "slotted." We use overlapping surfaces, generous whitespace (the "oxygen" of the layout), and high-contrast typography scales to create a premium, editorial flow that feels curated by a human hand, not a layout engine.

---

## 2. Colors & Tonal Architecture
The palette is a dialogue between warm linens and cool, desaturated greens. We do not use "pure" blacks or greys; every neutral is infused with a hint of organic pigment.

### The "No-Line" Rule
Traditional sectioning with 1px solid lines is strictly prohibited. Professionalism is conveyed through **chromatic boundaries**. To separate a header from a body section, transition from `surface` (#fef9f1) to `surface-container-low` (#f8f3eb). This creates a "soft edge" that feels integrated and expansive.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, fine-milled papers. 
*   **Base:** `surface` (#fef9f1) acts as the desk.
*   **Nesting:** Place `surface-container-lowest` (#ffffff) cards atop `surface-container` (#f2ede5) sections to create a crisp, natural lift. 
*   **Signature Textures:** For Hero sections or Primary CTAs, use a subtle linear gradient from `primary` (#36684f) to `primary-container` (#6b9e82) at a 135-degree angle. This adds "soul" and prevents the green from feeling flat or clinical.

---

## 3. Typography: The Editorial Voice
We utilize a sharp contrast between an expressive Serif and a functional Humanist Sans.

*   **Display & Headings (Newsreader):** This is our "Botanist’s Voice." Use `display-lg` (3.5rem) for hero titles. Tighten the letter-spacing (-0.02em) for larger sizes to increase the "ink-on-paper" feel.
*   **Body & UI (Manrope):** This is our "Scientific Clerk." Use `body-lg` (1rem) for long-form reading with a generous line-height (1.6) to ensure the text feels airy. 
*   **Hierarchy as Identity:** Always lead with a large `display-md` headline, followed by a `title-sm` in all-caps Manrope with 0.1em letter-spacing to act as a "pre-header" or "eyebrow" text.

---

## 4. Elevation & Depth: Atmospheric Layering
We move away from the "drop shadow" of the early 2010s toward **Atmospheric Perspective**.

*   **The Layering Principle:** Depth is achieved by stacking `surface-container` tiers. A `surface-container-highest` element should feel "closer" to the reader than a `surface-dim` element.
*   **Ambient Shadows:** If a floating element (like a modal) is required, use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(74, 60, 50, 0.06)`. The tint is Warm Brown, not grey, ensuring the shadow looks like a natural cast light on linen.
*   **Glassmorphism:** For top navigation bars or floating action menus, use `surface` at 80% opacity with a `backdrop-blur: 12px`. This allows the botanical imagery and colors of the journal to bleed through, softening the interface.
*   **The "Ghost Border":** If a container requires a boundary (e.g., in high-density data), use `outline-variant` (#c0c9c1) at 20% opacity. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** `primary` (#36684f) background with `on-primary` (#ffffff) text. Use `rounded-md` (0.75rem). No shadow; use a subtle scale-up (1.02x) on hover.
*   **Secondary:** `secondary-container` (#cae7d2) background. This should feel like a soft "leaf" against the linen background.
*   **Tertiary:** Text-only in `primary`. Use an underline that is `outline-variant` and 2px thick, offset by 4px.

### Cards & Lists
*   **The "No Divider" Rule:** Forbid horizontal lines between list items. Use 24px–32px of vertical white space or a subtle background shift to `surface-container-low` on hover.
*   **Cards:** Use `rounded-lg` (1rem) and `surface-container-lowest` (#ffffff). Cards should never have a shadow unless they are actively being "picked up" (dragged).

### Input Fields
*   **Styling:** Inputs should not be boxes, but "fields." Use a `surface-container-highest` background with a `rounded-sm` corner.
*   **Focus State:** Transition the "Ghost Border" from 20% to 100% opacity using `primary` (#36684f).

### Custom Component: The "Specimen Chip"
Used for plant categories or tags. A `secondary-fixed` (#cde9d5) pill with `on-secondary-fixed-variant` (#344c3d) text. The shape should be `rounded-full` to contrast against the more architectural cards.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins. If the left margin is 80px, try a right margin of 120px for editorial imagery.
*   **Do** allow images to "break the container." A botanical illustration should overlap two different surface tiers to knit the layout together.
*   **Do** use `Deep Sage` for all body text that sits on `Mint Dew` backgrounds to maintain accessible contrast.

### Don’t:
*   **Don’t** use pure black (#000000). Use `Warm Brown` (#4A3C32) for all dark text to maintain the organic warmth.
*   **Don’t** use hard 1px borders to "box in" content. Let the whitespace define the limits.
*   **Don’t** use standard "Material" ripple effects. Use soft fades (200ms ease-out) for interactions to maintain the "airy" feel.