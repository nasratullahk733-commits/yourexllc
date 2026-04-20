# Design System Strategy: The Monochromatic Architect

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Monochromatic Architect."** 

This system rejects the "template" aesthetic of modern e-commerce in favor of a high-end editorial experience. It draws inspiration from brutalist architecture and luxury fashion lookbooks, where prestige is communicated through massive scale, intentional asymmetry, and the mastery of light and shadow. By stripping away the crutch of color, we force the user to focus on form, product photography, and a sophisticated typographic rhythm. This is not just a shop; it is a curated digital gallery for 'yourexllc'.

## 2. Colors & Tonal Depth
The palette is a disciplined exploration of the grayscale spectrum. It relies on the interplay between deep obsidian and crystalline whites to create a sense of expensive permanence.

### The "No-Line" Rule
To achieve a premium feel, **1px solid borders are strictly prohibited for sectioning.** Conventional "boxes" make a site look like a template. Instead, define boundaries through:
*   **Tonal Shifts:** Transitioning from `surface` (#f9f9f9) to `surface_container_low` (#f3f3f4).
*   **Negative Space:** Using the Spacing Scale to create "invisible" borders.
*   **Value Contrast:** High-contrast blocks (e.g., a `primary` #000000 section directly abutting a `surface` #f9f9f9 section).

### Surface Hierarchy & Nesting
Treat the UI as physical layers of stacked material. 
*   **Base:** `surface` (#f9f9f9).
*   **The Layering Principle:** To highlight a product card or a floating UI element, use `surface_container_lowest` (#ffffff) to create a "lift" against the slightly darker `surface_container`. This provides a natural, soft depth that feels structural rather than decorative.

### The "Glass & Gradient" Rule
Flat black can often feel "dead" on digital screens. To inject "soul," use subtle gradients. For hero backgrounds or primary call-to-actions, apply a linear gradient from `primary` (#000000) to `primary_container` (#3b3b3b). For overlays, utilize Glassmorphism: semi-transparent `surface` colors with a 20px–40px backdrop-blur to allow product imagery to bleed through the UI subtly.

## 3. Typography: The Editorial Voice
Typography is the primary vehicle for the brand’s authority. This system utilizes a high-contrast scale to create an "Editorial Hierarchy."

*   **Display & Headlines (Manrope):** These are the "hero" elements. Use `display-lg` (3.5rem) for main product categories. The tight kerning and geometric precision of Manrope communicate modernity.
*   **Body & Labels (Inter):** Inter provides a technical, professional counter-balance. Its high legibility at `body-md` (0.875rem) ensures that product specifications and logistics are communicated with absolute clarity.
*   **The Hierarchy Strategy:** Pair oversized `display-md` headlines with significantly smaller `label-md` uppercase sub-headers to create the "high-low" contrast typical of luxury magazine layouts.

## 4. Elevation & Depth: Tonal Layering
In a strictly black-and-white system, traditional drop shadows can often look "dirty." We replace them with **Ambient Tonal Layering**.

*   **The Layering Principle:** Instead of a shadow, place a `surface_container_highest` (#e2e2e2) element on a `surface` (#f9f9f9) background. The change in value creates the "step" in height.
*   **Shadow Exception:** If a floating element (like a cart drawer) requires a shadow, it must be an "Ambient Shadow": 
    *   Color: `on_surface` (#1a1c1c) at 4% opacity.
    *   Blur: 40px–80px.
    *   Spread: -10px. 
    *   This creates a soft, architectural glow rather than a harsh "drop shadow."
*   **Sharpness as Luxury:** With a **0px Roundedness Scale**, every element is perfectly rectilinear. This architectural "sharp edge" communicates precision and high-end engineering.

## 5. Components

### Navigation: The Signature Hamburger
The navigation is housed behind a minimalist 3-line hamburger menu in the header. 
*   **Style:** Lines should be 1.5px thick using `primary` (#000000). 
*   **Interaction:** Upon clicking, the menu should expand into a full-screen `surface_container_lowest` (#ffffff) overlay, utilizing `display-sm` Manrope typography for the links.

### Buttons (The "Sharp" CTA)
*   **Primary:** Solid `primary` (#000000) with `on_primary` (#e2e2e2) text. 0px border-radius.
*   **Secondary:** Ghost style. No border. Use `on_surface` text with a `primary_container` (#3b3b3b) hover state at 5% opacity.
*   **Tertiary:** `label-md` uppercase with a 1px `primary` underline, spaced 4px from the text.

### Input Fields
*   **Style:** No 4-sided boxes. Use a bottom-only border (1px) using `outline_variant` (#c6c6c6). 
*   **State:** On focus, the border transitions to `primary` (#000000) with a 2px thickness.

### Cards & Product Lists
*   **Rule:** Forbid divider lines. 
*   **Design:** Separate product items using `surface_container_low` backgrounds or generous white space. Imagery should be the "anchor," with `title-sm` text placed with intentional asymmetry (e.g., left-aligned title, right-aligned price).

### Chips & Tags
*   **Design:** Use `surface_container_highest` (#e2e2e2) backgrounds with `on_surface_variant` (#474747) text. Keep them rectangular (0px) to maintain the architectural theme.

## 6. Do's and Don'ts

### Do:
*   **Embrace Asymmetry:** Place text off-center or overlapping images (using tonal contrast to ensure readability).
*   **Use Massive Whitespace:** Luxury is defined by the "waste" of space. Give every element room to breathe.
*   **Strict Adherence to 0px:** Even a 1px radius will break the sophisticated, high-end "Architect" look.

### Don't:
*   **Don't Use "Grey" for Text:** Use `on_surface` (#1a1c1c) for maximum legibility. Only use `on_surface_variant` for metadata.
*   **Don't Add Borders:** If you feel the need to separate content, increase the padding or shift the background color to `surface_container`.
*   **Don't Use Color:** This system is strictly monochromatic. Use photography to introduce color; the UI must remain a neutral, sophisticated frame.

### Accessibility Note
While maintaining a minimalist look, ensure that `error` (#ba1a1a) is used sparingly for critical feedback (e.g., incorrect credit card info). Even here, the error state should follow the sharp-edged, no-border philosophy.