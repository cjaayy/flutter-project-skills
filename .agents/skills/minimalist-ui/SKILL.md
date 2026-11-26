---
name: minimalist-ui
description: Enforce strict monochrome grey minimalist Flutter UI rules, hand-crafted Iconoir bare grey unique icons, zero custom-drawn SVG icons, zero emojis, maroon-red delete buttons, colorless standard buttons, and overflow-free mobile alignment. Use whenever creating, editing, or styling any Flutter screen, widget, layout, button, card, or form.
---

# Minimalist Monochrome Grey UI (Flutter)

## 1. Color & Visual Discipline
- **Grey Monochrome Only:** Keep the entire interface strictly grey and neutral monochrome (white, black, and neutral grey shades) until the user explicitly specifies a color or custom design.
- **No Unsolicited Styling:** Do not add random designs, decorative gradients, background tints, or colorful accents on your own.

## 2. Icons & Zero Emojis
- **Locked Hand-Crafted Library (Iconoir):** Use **`iconoir_flutter`** exclusively for all icons so every icon looks human-crafted, architectural, and distinct from generic AI templates.
- **No AI-Drawn Custom Icons or Generic Defaults:** Never draw custom icon paths via `CustomPainter` or raw SVG strings, and never use default `Icons.*` material icons when an `iconoir_flutter` icon fits.
- **Unique Bare Grey Icons:** Assign a distinct, semantically accurate icon to every action, navigation item, or section - never recycle the same icon for different functions. Render all icons in plain neutral grey only (`Color(0xFF737373)`) at uniform size (`18`-`20`), with zero background color, circle, or box container behind them.
- **Strict Zero-Emoji Rule:** Never use emojis anywhere in widget text, headings, labels, buttons, hints, or snackbars.

## 3. Cards & Badges
- **No Unrequested Badges:** Do not add badges, chips, or status pills unless explicitly requested by the user.
- **No Card Background Colors:** Do not apply background fill colors to cards unless explicitly instructed. Keep cards flat and clean using minimal borders or spacing only.

## 4. Button Rules
- **Delete Buttons:** Style delete or destructive action buttons in **maroon red** (`Color(0xFF800000)`) paired with an Iconoir trash/delete icon.
- **All Other Buttons:** Keep every other button completely colorless (neutral grey/black/white text and subtle neutral border only). Never use blue, green, or bright accent colors on standard buttons unless instructed.

## 5. Responsive & Alignment Guardrails
- **Zero Overflow Across All Phone Sizes:** Wrap screens in `SafeArea` and use `Expanded`, `Flexible`, or scrollable containers so no `RenderFlex overflow` occurs on compact or large phone viewports.
- **Re-Align on Every Addition:** Whenever adding new widgets, buttons, inputs, or sections, check and adjust surrounding constraints immediately so alignment stays clean across devices.
