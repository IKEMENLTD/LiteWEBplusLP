# LiteWEB+ Design Specification (Blue Avant-Garde)

## 1. Design Concept
**Theme:** Blue Avant-Garde Tech
**Keywords:** Intellectual, Disruptive, Fluid, High-Contrast, Future-Oriented
**Core Visuals:**
- **Deep Navy & Pale Blue:** A sophisticated, monochromatic base that feels both professional and futuristic.
- **Electric Blue Accent:** A vivid, digital blue that cuts through the calmness to create impact.
- **Mega Typography:** Typography treated as a graphic element, with outlines and massive scaling.
- **Broken Grid:** Asymmetrical layouts that challenge traditional web structures.
- **Fluid & Noise:** Background textures that add depth and "air" to the digital space.

## 2. Color Palette
| Variable | Color Code | Description |
| :--- | :--- | :--- |
| `--c-bg` | `#F0F6FF` | **Pale Blue**. The main background. Clean, airy, and modern. |
| `--c-surface` | `#FFFFFF` | **White**. Used for cards and content areas to create depth. |
| `--c-ink` | `#00204A` | **Deep Navy**. The primary text color. Intelligent and sharp. |
| `--c-ink-light` | `#4B6584` | **Muted Blue-Grey**. Used for secondary text and borders. |
| `--c-accent` | `#0057FF` | **Electric Blue**. The primary action color. Vibrant and energetic. |

## 3. Typography
**Display Font:** `Outfit` (Google Fonts)
- Weights: 600, 800
- Usage: Headings, Hero Text, Navigation, Buttons, Numbers.
- Style: Uppercase, Tight Letter Spacing (-0.04em), High Contrast.

**Body Font:** `Noto Sans JP` (Google Fonts)
- Weights: 400, 500, 700
- Usage: Paragraphs, UI Text, Japanese Content.
- Style: Clean, Legible, Modern.

## 4. UI Components

### Buttons (`.circle-btn`)
- **Shape:** Geometric Polygon (Hexagon-like).
- **Style:** Solid Electric Blue background with white text.
- **Interaction:** Hovers to Deep Navy background, slight translation, and shadow expansion.
- **Shadow:** Hard drop shadow in Deep Navy.

### Cards (`.pricing-card`, `.target-card`)
- **Style:** White or Deep Navy background with sharp corners (radius 4px).
- **Border:** Minimal or none.
- **Shadow:** Large, soft colored shadows for "Creative" plans; hard shadows for others.
- **Interaction:** Lift up on hover.

### Navigation (`.nav-fixed`)
- **Layout:** Distributed (Logo top-left, Menu button top-right, CTA bottom-right).
- **Style:** Fixed position, floating elements.
- **Menu:** Full-screen Deep Navy overlay with massive centered links.

### Animations
- **Reveal:** Text slides up from a masked container (`.reveal-text`).
- **Char Reveal:** Each character fades and slides in sequentially (`.char-reveal`).
- **Marquee:** Continuous scrolling text strip for clients/partners.
- **Fluid Background:** Subtle noise and moving gradient blobs.

## 5. Responsive Guidelines
- **Mobile First:** All layouts stack vertically on mobile.
- **Typography:** `clamp()` based scaling ensures text is massive on desktop but readable on mobile.
- **Tables:** Convert to block-level elements on mobile for readability.
- **Navigation:** Simplified to Logo and Menu Button on mobile.

## 6. Implementation Notes
- **Hero Visibility:** Hero text must have `z-index: 50` and `text-shadow` to ensure visibility over the video.
- **Performance:** Use `will-change` for complex animations.
- **Accessibility:** Ensure high contrast between text (Navy) and background (Pale Blue/White).
