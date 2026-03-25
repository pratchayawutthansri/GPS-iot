# Design System Document

## 1. Overview & Creative North Star: "The Living Pulse"
This design system moves beyond the cold, clinical nature of traditional IoT interfaces to create an experience that feels as vital and organic as the pets it protects. Our Creative North Star is **"The Living Pulse"**—a philosophy that balances high-precision data with a soft, editorial human touch. 

To break the "template" look of standard web apps, this system rejects rigid grids in favor of **intentional asymmetry** and **tonal layering**. We treat the UI not as a flat screen, but as a series of tactile, "living" surfaces. High-contrast typography scales (the juxtaposition of the geometric Manrope and the functional Inter) create an authoritative yet approachable voice, ensuring the user feels they are using a premium, tech-forward tool that prioritizes their pet’s well-being.

---

## 2. Colors & Surface Philosophy
The palette is anchored by a vibrant, minty "Tech Green" (`primary`) and a sophisticated "Deep Sea" (`tertiary`), supported by a sophisticated range of cool grays.

### The "No-Line" Rule
To achieve a premium, custom feel, **1px solid borders for sectioning are strictly prohibited.** Boundaries must be defined solely through background color shifts. For example:
- A `surface-container-low` (#eef1f0) card sitting on a `surface` (#f4f7f6) background.
- This creates a seamless, "molded" look that feels integrated into the hardware-software ecosystem.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of materials. 
- **Level 0 (Base):** `surface` (#f4f7f6)
- **Level 1 (Sections):** `surface-container` (#e5e9e8)
- **Level 2 (Active Cards):** `surface-container-lowest` (#ffffff)
Use these tiers to create "nested" depth. An inner data visualization container should sit on a `surface-container-high` (#dee3e2) area to pull the user’s eye inward without the clutter of lines.

### The Glass & Gradient Rule
Floating elements (modals, navigation bars) should utilize **Glassmorphism**. Apply `surface` colors at 70% opacity with a `backdrop-blur` of 20px. 
**Signature Textures:** For Hero sections or primary CTAs, use a subtle linear gradient from `primary` (#006857) to `primary-container` (#50f5d5) at a 135-degree angle. This adds "visual soul" and a sense of energy that flat colors lack.

---

## 3. Typography: The Editorial Contrast
We use a dual-typeface system to balance technical precision with a friendly, trustworthy "Pet-Parent" tone.

*   **Display & Headlines (Manrope):** Chosen for its modern, geometric construction and high legibility. Use `display-lg` (3.5rem) for hero moments to create a bold, editorial impact.
*   **Body & Labels (Inter):** A functional workhorse. Use `body-md` (0.875rem) for data readouts and descriptions. 

**Visual Hierarchy Tip:** Always pair a large `headline-md` (Manrope) with a significantly smaller `label-md` (Inter) in `on-surface-variant` (#585c5c) for metadata. This "Big-Small" contrast is the hallmark of high-end digital design.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to represent "importance"; we use light and layering.

*   **The Layering Principle:** Depth is achieved by "stacking" surface-container tiers. A white card (`surface-container-lowest`) on a light gray base (`surface`) creates a natural lift.
*   **Ambient Shadows:** If a floating element (like a pet-profile popover) requires a shadow, it must be "Ambient": `box-shadow: 0 20px 40px rgba(43, 47, 47, 0.06)`. The shadow color is a tinted version of `on-surface`, never pure black.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility in input fields, use `outline-variant` (#aaaead) at **20% opacity**. Never use a 100% opaque border.

---

## 5. Components

### Buttons & Chips
*   **Primary Button:** Uses the signature `primary` to `primary-container` gradient. Corner radius: `xl` (1.5rem / 24px) for a friendly, pill-like feel.
*   **Secondary/Ghost Button:** `surface-container-highest` (#d8dedd) background with `on-surface` text. No border.
*   **Status Chips:** Use `tertiary-container` (#09c4fd) for active tracking states. These should have a "Glass" effect when placed over imagery.

### Cards & Lists
*   **Cards:** Use `lg` (1rem / 16px) or `xl` (1.5rem / 24px) roundedness. 
*   **List Items:** **Forbid divider lines.** Separate items using `2` (0.5rem) vertical spacing and a subtle background hover state shift to `surface-container-high`.

### Inputs & Interaction
*   **Input Fields:** Background: `surface-container-low` (#eef1f0). Focus state: A "Ghost Border" of `primary` at 40% opacity and a subtle 2px inner glow.
*   **IoT "Live" Indicator:** A small `primary` circle with a soft, pulsing `primary-container` shadow to indicate real-time data sync.

### Bespoke IoT Components
*   **Vitality Ring:** A circular progress component using `primary` for "Health" and `tertiary` for "Activity," layered over a `surface-variant` track.
*   **Safe-Zone Map Container:** A `xl` rounded container with a `backdrop-blur` overlay for the map controls, making the tech feel integrated into the environment.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins (e.g., more whitespace on the left than the right in hero sections) to create a custom, designed feel.
*   **Do** use `surface-tint` (#006857) at very low opacities (3-5%) as an overlay for image-heavy cards to unify the visual tone.
*   **Do** prioritize "Breathing Room" using the top end of the spacing scale (`16`, `20`, `24`).

### Don't:
*   **Don't** use 1px solid dividers to separate content. Use whitespace or tonal shifts.
*   **Don't** use standard "drop shadows" with high opacity. They break the soft minimalism.
*   **Don't** use sharp corners. Everything must adhere to the `lg` to `xl` roundedness scale to maintain the "friendly" brand promise.
*   **Don't** use pure black (#000000) for text. Use `on-surface` (#2b2f2f) to keep the contrast soft and accessible.