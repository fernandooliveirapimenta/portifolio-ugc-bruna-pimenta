# Editorial Elegance: A Custom Design System for the Digital Creator

## 1. Overview & Creative North Star

### Creative North Star: "The Digital Curator"
This design system is built to bridge the gap between traditional high-end editorial magazines and modern digital storytelling. It rejects the "standard" SaaS interface in favor of a curated gallery aesthetic. We move beyond templates by embracing **intentional asymmetry**, high-contrast typographic scales, and a tactile sense of depth.

The system is designed to position a creator not just as a service provider, but as a premium brand. It achieves this through "Soft Minimalism"—where the luxury is felt in the breathing room (negative space) and the precision of the typography rather than decorative flourishes.

---

## 2. Colors

The palette is a sophisticated range of warm neutrals and "ink" tones, designed to make photography and video content the focal point.

### Tonal Foundations
- **Background (`#fffbff`):** A crisp, slightly warm paper white that provides a clean slate.
- **On-Background/Surface (`#39382c`):** Our "ink" color. Never use pure black; this charcoal-olive blend feels softer and more expensive.
- **Primary Foundation (`#625e59`):** A muted taupe used for key interactive elements.

### The "No-Line" Rule
To maintain the editorial feel, **1px solid borders are prohibited for sectioning.** Boundaries between content blocks must be defined solely through background color shifts.
*   *Example:* A section using `surface_container_low` (`#fdf9ef`) sitting directly on a `background` (`#fffbff`) creates a "block" without the rigidity of a line.

### Surface Hierarchy & Nesting
Treat the UI as a series of layered fine-paper sheets. Use the surface-container tiers to create depth:
1.  **Level 0 (Background):** `surface`
2.  **Level 1 (Sections):** `surface_container_low`
3.  **Level 2 (Cards/Modules):** `surface_container_lowest` or `surface_bright` to create a soft "pop."

### Signature Textures
Avoid flat, "dead" blocks of color. For hero sections or primary CTAs, utilize a subtle gradient transition from `primary` (`#625e59`) to `primary_container` (`#e8e1db`) to provide visual soul and a tactile, light-catching quality.

---

## 3. Typography

The typography is the backbone of this system’s authority. It relies on the interplay between a classic Serif and a technical Sans-Serif.

### The Serif: Noto Serif (Editorial Authority)
Used for all `display` and `headline` levels. This font conveys heritage and professional curation. 
- **Character Spacing:** Set `display-lg` and `display-md` to -0.02em tracking for a tighter, more "masthead" appearance.
- **Usage:** Quotes, section headers, and the creator's name.

### The Sans: Manrope (Modern Precision)
Used for `title`, `body`, and `label` levels. Manrope is highly legible and provides a functional counterpoint to the Serif.
- **Body-LG (`1rem`):** The workhorse for storytelling. Ensure line height is set to at least 1.6 for maximum readability.
- **Label-MD (`0.75rem`):** Use for technical data or categories, often in all-caps with +0.05em tracking for a "labeled" look.

---

## 4. Elevation & Depth

We eschew the heavy shadows of traditional material design in favor of **Tonal Layering**.

### The Layering Principle
Depth is achieved by stacking. A `surface_container_highest` (`#ece8d7`) element on a `surface` background provides enough contrast to imply elevation without a single pixel of shadow.

### Ambient Shadows
When a "floating" effect is necessary (e.g., a video preview card or a navigation bar):
- **Blur:** 40px to 60px.
- **Opacity:** 4% - 6%.
- **Color:** Use a tinted version of `on_surface` (`#39382c`) rather than black. This ensures the shadow feels like a natural part of the environment.

### Glassmorphism & Depth
For floating menus or mobile overlays, use `surface_container_lowest` at 80% opacity with a `backdrop-filter: blur(12px)`. This creates a "frosted glass" effect that allows the warm beige tones of the background to bleed through, softening the layout.

---

## 5. Components

### Buttons
- **Primary:** Filled with `primary` (`#625e59`), text in `on_primary` (`#fef6f0`). 
- **Secondary:** Outlined using the **Ghost Border** (10% opacity of `outline`) with `primary` text.
- **Shape:** Use the `full` (pill) roundedness scale for a soft, approachable feel.

### Video & Photo Cards
- **Corners:** Use `xl` (`1.5rem`) for video previews and `md` (`0.75rem`) for smaller static images.
- **Interaction:** On hover, cards should slightly lift using an **Ambient Shadow**, never a border.

### Input Fields
- **Style:** Underline only or extremely subtle `surface_container` fills. 
- **Error States:** Use `error` (`#a54731`) for text, but avoid bright red boxes. Keep the error messaging elegant and minimal.

### Content Chips
- Use `surface_container_high` for the background with `on_surface` text.
- **Rule:** No dividers between chips. Use the `DEFAULT` (`0.5rem`) spacing scale to let them breathe.

### Signature Component: The "Editorial Stat"
For social media metrics or case studies, use `display-md` for the number and `label-sm` (all caps) for the description, stacked vertically with zero ornamentation.

---

## 6. Do's and Don'ts

### Do:
- **Embrace White Space:** If a section feels crowded, double the padding. High-end brands "waste" space intentionally.
- **Asymmetric Grids:** Offset images from text blocks to create a dynamic, magazine-style layout.
- **Tonal Transitions:** Use background shifts to guide the user's eye from one content pillar to the next.

### Don't:
- **Don't use Dividers:** Never use a horizontal line to separate sections. Use a `surface` color shift instead.
- **Don't use High Contrast Shadows:** Avoid the "floating box" look. Shadows should be felt, not seen.
- **Don't use Pure Black:** Keep all text and UI lines within the `on_surface` or `primary` palettes to maintain the warm, professional mood.
- **Don't use Default Border Radii:** Stick strictly to the defined Roundedness Scale to ensure the "curated" feel remains consistent across all modules.