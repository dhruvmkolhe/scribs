# Hand-Drawn Creative Studio — Website Design & Development Prompt

## Project Overview

Create a playful, human-centered website inspired by hand-drawn illustrations, paper textures, sticky notes, and creative brainstorming sessions.

The design should embrace authentic imperfection, organic shapes, handwritten typography, and intentional asymmetry. It should feel like a creative sketchbook brought to life rather than a conventional, polished digital interface.

Prioritize approachability, creativity, personality, and ease of interaction. Every element should feel thoughtfully handmade, with a consistent visual language that celebrates imperfection.

## 1. Design System

### Color Palette

Use the following light-mode color palette throughout the website.

| Token | Color | Usage |
|---|---|---|
| Background | `#fdfbf7` | Warm paper background |
| Foreground | `#2d2d2d` | Soft pencil black |
| Muted | `#e5e0d8` | Old paper and erased pencil |
| Accent | `#ff4d4d` | Red correction marker |
| Border | `#2d2d2d` | Pencil lead |
| Secondary Accent | `#2d5da1` | Blue ballpoint pen |
| White | `#ffffff` | Card and button backgrounds |
| Post-it Yellow | `#fff9c4` | Feature cards and sticky-note accents |

Maintain a cohesive, limited color palette. Avoid introducing additional colors that conflict with the handmade aesthetic.

### Typography

Use handwritten fonts exclusively.

- Headings: Kalam, font weight 700.
- Body text: Patrick Hand, font weight 400.
- Maintain large, readable typography with dramatic differences in size.
- Use bold, marker-like headings to emphasize important content.
- Keep body text approachable and legible.

Typography should feel natural and expressive, like handwritten notes on paper.

## 2. Organic Shapes & Wobbly Borders

### Core Principle

No straight lines. Every container, button, card, and image frame should use irregular, organic border-radius values rather than standard geometric shapes.

Do not rely on standard Tailwind rounded classes alone.

Use custom inline border-radius values or reusable design tokens to create asymmetrical, hand-drawn edges.

### Border-radius tokens

Store reusable values in the configuration as `wobbly` and `wobblyMd`.

Example:

```css
border-radius: 255px 15px 225px 15px /
               15px 225px 15px 255px;
```

Apply the wobbly radius values consistently across the interface while varying them enough to maintain an authentic, handmade appearance.

### Borders
- Minimum border width: 2px.
- Use 3px or 4px borders for important elements.
- Default border style: solid.
- Use dashed borders for secondary elements, dividers, and decorative sketch overlays.
- Keep border color consistent with the pencil-black palette.

## 3. Paper Texture & Visual Effects

### Background Texture

Apply a subtle radial-gradient dot pattern to the body background to simulate notebook paper grain.

```css
background-image: radial-gradient(
  #e5e0d8 1px,
  transparent 1px
);
background-size: 24px 24px;
```

Keep the texture subtle enough to preserve readability and avoid visual clutter.

### Hard Offset Shadows

Use solid, offset shadows to create a layered paper collage effect.

Never use soft or blurred shadows.

Standard shadow:

```css
box-shadow: 4px 4px 0px 0px #2d2d2d;
```

Emphasized shadow:

```css
box-shadow: 8px 8px 0px 0px #2d2d2d;
```

Hover shadows should reduce the offset to create a lifting effect.

### Paper Decorations

Use visual elements inspired by physical media:

- Translucent tape strips.
- Colored thumbtacks.
- Hand-drawn arrows.
- Dashed lines and irregular shapes.
- Sticky-note labels.
- Scribbled circles and underlines.
- Paper textures and overlapping layers.

Keep decorations intentional and avoid overcrowding the layout.

## 4. Navigation & Header

Create a minimal, playful navigation system.

- Use handwritten typography for navigation labels.
- Apply wavy underline decorations to navigation links.
- Introduce subtle rotations and irregular shapes where appropriate.
- Keep interactive elements visually distinct and easy to identify.

Maintain a consistent hand-drawn aesthetic across desktop and mobile layouts.

## 5. Hero Section

Create an expressive, visually engaging hero section.

### Layout
- Use a two-column layout on desktop.
- Stack the content vertically on mobile.
- Use generous whitespace and asymmetrical alignment.
- Keep the main content within a `max-w-5xl` container.

### Typography
Use large, handwritten headings with dramatic size variations.

Include a playful exclamation mark in the hero headline and apply a slight rotation to reinforce the handmade personality.

### Decorations
- Add a hand-drawn arrow pointing toward the primary CTA.
- Include a bouncing decorative circle near the hero image on desktop.
- Use corner frame marks around the hero image placeholder.
- Apply subtle rotations to images and decorative elements.

Hide the decorative arrow and bouncing circle on mobile.

## 6. Buttons & Interactive Elements

### Primary Button

Create an irregular, wobbly oval button using the reusable `wobbly` border-radius token.

Normal state:
- White background.
- 3px solid pencil-black border.
- Pencil-black text.
- Patrick Hand typography.
- Hard offset shadow of `4px 4px 0px 0px #2d2d2d`.

Hover state:
- Background changes to correction-marker red `#ff4d4d`.
- Text changes to white.
- Shadow reduces to `2px 2px 0px 0px #2d2d2d`.
- Translate the button by 2px horizontally and vertically.

Active state:
- Remove the shadow completely.
- Translate the button by 4px horizontally and vertically.
- Make the button feel as though it is physically pressing into the paper.

### Secondary Button

Use a muted background of `#e5e0d8`.

On hover, transition to the blue ballpoint color `#2d5da1`.

Maintain the same wobbly shape and hard-shadow interaction.

### Accessibility

- Minimum button height: 48px.
- Maintain adequate spacing between interactive elements.
- Ensure visible focus states and clear interactive feedback.

## 7. Cards & Containers

### Base Style

- White background.
- 2px solid pencil-black border.
- Custom `wobblyMd` border-radius.
- Subtle hard shadow: `3px 3px 0px 0px rgba(45, 45, 45, 0.1)`.

### Decoration Options

Support the following decorative variations:

Tape:
A translucent gray strip positioned at the top center of the card, with a slight rotation.

Tack:
A small red circular thumbtack positioned at the top center.

Minimal:
No additional decoration.

### Special Card Treatments

- Use post-it yellow `#fff9c4` for feature cards.
- Add speech-bubble tails to testimonial cards using a border-based triangle.
- Apply slight rotations to selected cards.
- Allow intentional overlap between decorative elements and containers.

### Hover Interactions

- Rotate cards slightly using `hover:rotate-1` or `hover:-rotate-1`.
- Increase shadow offset on blog cards to create a lifting effect.
- Use quick, playful transitions.

## 8. Inputs & Forms

Create form elements that feel like handwritten notes on paper.

### Input Styling
- White background.
- 2px border using the pencil-black color.
- Custom wobbly border-radius.
- Patrick Hand typography.
- Muted placeholder text using pencil-black at 40% opacity.

### Focus State
- Change the border to blue `#2d5da1`.
- Add a subtle blue ring using `ring-2 ring-[#2d5da1]/20`.
- Avoid standard rectangular outlines.
- Preserve the organic shape of the input.

## 9. Layout & Composition

### Grid System

Use Tailwind's responsive grid system while introducing intentional visual irregularity.

- Two-column grids: `md:grid-cols-2`.
- Three-column grids: `md:grid-cols-3`.
- Four-column stats: `md:grid-cols-4`.
- Single-column layouts on mobile unless otherwise specified.

### Spacing
- Section padding: `py-20`.
- Grid gaps: `gap-8`.
- Focused content: `max-w-5xl` or `max-w-3xl`.
- Reduce horizontal padding to `px-6` when needed on mobile.

### Breaking Alignment

Introduce visual variety through:

- Slightly rotated cards and images.
- Irregularly shaped statistic containers.
- Overlapping avatar circles using `-space-x-4`.
- Decorative elements positioned outside their parent containers.
- Intentional asymmetry in image placement.
- Slightly enlarged highlighted pricing cards using `md:scale-105`.

Avoid making the layout feel mechanically aligned or overly uniform.

## 10. Unique Visual Signatures

Use the following hand-drawn details to establish a distinctive design identity.

### Hand-Drawn SVG Decorations
- A dashed arrow pointing toward the hero CTA.
- A squiggly connecting line between the steps in the How It Works section.
- Corner frame marks around the hero image placeholder.

### Authentic Paper Effects
- Tape strips on feature cards.
- Thumbtack pins on selected cards.
- Dashed circle overlays around the popular pricing tier.
- Speech-bubble tails on testimonials.
- Sticky-note tags for section labels.

### Playful Typography
- Rotating exclamation mark in the hero headline.
- Wavy underlines on navigation links and footer headings.
- Drop-cap first letter treatment in the Product Detail section.
- Post-it yellow sticky-note tag on the Product Detail card.

### Scribbled Accents
- Bouncing decorative circle near the hero image.
- Dashed borders on secondary elements and dividers.
- Emoji sketches in blog post placeholders.
- Hand-drawn circles and arrows to emphasize important information.

## 11. Interactive Personality

Make interactions feel playful, responsive, and physically connected to the interface.

- Buttons should press flat when activated.
- Cards should rotate slightly on hover.
- Blog cards should increase their hard-shadow offset when lifted.
- Navigation links should feature hand-drawn underline effects.
- Decorative elements should use gentle bounce animations with a 3-second duration.
- Apply subtle rotation on hover where appropriate.

Use `transition-transform duration-100` for fast, playful interactions.

Remove the grayscale-to-color transition on blog images. Keep images in their original colors for the final implementation.

## 12. Responsive Design

Adopt a mobile-first approach while preserving the core hand-drawn aesthetic across all screen sizes.

### Typography

Use responsive typography such as:

- Headings: `text-4xl md:text-5xl` or `text-5xl md:text-6xl`.
- Body text: `text-lg md:text-xl` or `text-base md:text-xl`.
- Buttons: `text-lg md:text-2xl`.

### Layout
- Collapse all grids to a single column on mobile, except the stats grid.
- Use two-column or three-column grids from the `md` breakpoint onward.
- Stack the hero section vertically on mobile.
- Display stats in two columns on mobile and four columns on desktop.
- Scale down pricing cards to `p-6 md:p-8`.

### Decorative Elements

Hide the following decorative elements on mobile:

- Hand-drawn arrow near the CTA.
- Bouncing decorative circle.
- Squiggly connecting line in the How It Works section.
- Dashed circle surrounding the popular pricing tier.

Reduce rotations slightly when necessary, using `-rotate-1` instead of `-rotate-2`.

### Maintain the Core Aesthetic

- Preserve wobbly borders and handwritten fonts.
- Keep hard offset shadows without blur.
- Maintain playful shapes and irregular alignment.
- Ensure buttons remain at least 48px tall.
- Maintain adequate spacing between interactive elements.
- Preserve section padding of `py-20`, reducing horizontal padding when needed.

For stats, use `h-24 w-24 md:h-32 md:w-32`.

## 13. Implementation Requirements

- Use Tailwind CSS for layout, spacing, and responsive styling.
- Use Kalam and Patrick Hand as the primary typefaces.
- Define reusable `wobbly` and `wobblyMd` border-radius tokens.
- Use inline styles for irregular border-radius values where necessary.
- Use Lucide React icons with `stroke-width={2.5}` or `stroke-width={3}`.
- Enclose key icons in rough, hand-drawn circles.
- Use CSS transforms for rotation, lifting, and pressing interactions.
- Use CSS or SVG for hand-drawn decorative elements.
- Keep all shadows hard and offset, without blur.
- Maintain responsive layouts and accessible touch targets.

## Final Design Direction

The finished website should feel like a creative sketchbook, a brainstorming wall, or a collection of handwritten notes brought to life.

Embrace authentic imperfection, expressive typography, organic shapes, paper textures, and playful interactions.

The design should feel spontaneous and human-centered without sacrificing readability, usability, or responsive behavior.

Prioritize creativity over corporate polish. Every element should invite users to explore, interact, and feel like collaborators in an ongoing creative process.

Preserve all specified design details and interactions. Do not introduce unnecessary decorative elements or visual styles that conflict with the hand-drawn aesthetic.