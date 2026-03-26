```markdown
# Design System Strategy: The Academic Pulse

## 1. Overview & Creative North Star
This design system is engineered to bridge the gap between the ironclad authority of traditional Japanese media (Nikkei) and the fluid, high-velocity innovation of the tech sector. 

**Creative North Star: "The Digital Curator"**
The aesthetic is not a "template"—it is a high-end editorial experience. We reject the generic "SaaS-blue" look in favor of a sophisticated, layered environment that feels like a premium digital journal. We achieve this through:
*   **Intentional Asymmetry:** Breaking the 12-column rigidity with staggered content blocks.
*   **Tonal Depth:** Replacing harsh structural lines with soft shifts in background values.
*   **Authoritative Scale:** Using extreme contrast in typography sizes to command attention and establish an immediate information hierarchy.

---

## 2. Colors: Tonal Architecture
We utilize a sophisticated palette where "Nikkei Blue" serves as the anchor of trust, while vibrant tech-blue gradients provide the "pulse" of innovation.

### Surface Hierarchy & Nesting
To create a premium feel, we treat the UI as a series of physical layers—like stacked sheets of fine paper or frosted glass.
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for defining sections. Boundaries must be created through background color shifts.
*   **Nesting Logic:** 
    *   **Base:** `surface` (#fbf9f9)
    *   **Sectioning:** `surface-container-low` (#f5f3f3)
    *   **Interaction Cards:** `surface-container-lowest` (#ffffff)
*   **Glassmorphism:** For floating elements (menus, tooltips), use semi-transparent `surface` colors with a 12px-20px `backdrop-blur`. This allows the "Nikkei Blue" accents to bleed through, softening the tech-heavy interface.

### Signature Textures
Main CTAs and Hero backgrounds should never be flat. Use a linear gradient: 
`primary` (#005faf) → `primary_container` (#4d9dff) at a 135-degree angle. This adds "soul" and motion to the static page.

---

## 3. Typography: The Editorial Voice
Our typography balance conveys both "Academic Rigor" and "Modern Speed."

*   **Display & Headlines (Manrope / Noto Sans JP):** Use `headline-lg` and `display-sm` with a weight of 700 or higher. These should feel heavy and unavoidable, acting as the "anchor" for the page's trust factor.
*   **Body (Inter / Noto Sans JP):** Optimized for long-form reading. Use `body-md` (#414752) for primary content to reduce eye strain compared to pure black.
*   **Labels (Inter):** Use `label-md` in all-caps or with increased letter-spacing (0.05em) for a "technical data" aesthetic that feels precise and curated.

---

## 4. Elevation & Depth: Tonal Layering
Traditional structural lines make an interface feel "boxy" and dated. We use **Tonal Layering** to define space.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` background to create a "natural lift." The eye perceives the brighter white as being closer to the viewer.
*   **Ambient Shadows:** If a floating state is required (e.g., a hovered card), use an extra-diffused shadow: `box-shadow: 0 12px 40px rgba(0, 95, 175, 0.06);`. Note the blue tint in the shadow—this mimics natural light passing through a blue-themed environment.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.

---

## 5. Components: Precision & Fluidity

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary_container`), `DEFAULT` (0.5rem) rounded corners. No border.
*   **Secondary:** `surface-container-highest` background with `on-primary-fixed-variant` text. This creates a "low-impact" but professional alternative.
*   **Tertiary:** No background. Bold text in `primary` with a subtle `primary_fixed` underline on hover.

### Cards & Scout Items
*   **Restriction:** Forbid horizontal divider lines.
*   **Separation:** Use vertical white space (`Spacing 10` or `12`) or subtle background shifts.
*   **Interaction:** On hover, a card should shift from `surface-container-lowest` to a subtle `primary_fixed` (10% opacity) tint, rather than just getting a shadow.

### Input Fields
*   **Styling:** Use `surface-container-high` as the background. On focus, the background shifts to `surface-container-lowest` with a 2px `primary` bottom-border only. This mimics high-end stationery.

### Specialized Component: The Scout Pulse
For the "Scout Received" notification, use a `surface_bright` container with a glassmorphism backdrop blur and a thin `secondary_container` (#fe9c2a) accent bar on the left. This orange provides the "Excitement" factor against the calm blue background.

---

## 6. Do's and Don'ts

### Do
*   **DO** use whitespace as a functional tool. If elements feel crowded, increase the spacing scale rather than adding a divider.
*   **DO** use `Manrope` for numbers and tech-metrics. Its geometric shapes feel modern and high-speed.
*   **DO** experiment with overlapping elements (e.g., a profile image slightly breaking the boundary of its container) to create a custom, editorial feel.

### Don't
*   **DON'T** use #000000. It is too harsh for this "Academic" palette. Always use `on-surface` (#1b1c1c).
*   **DON'T** use 100% opaque borders. They create "visual noise" that contradicts the "Clean/Speed" goal.
*   **DON'T** use the `secondary` orange for large surfaces. It is a "spark" color meant for notifications, badges, and primary action highlights only.

---
**Director's Note:** Every pixel must feel intentional. If an element exists, it must have a clear tonal reason for being there. This is not a UI; it is an environment for career growth.```