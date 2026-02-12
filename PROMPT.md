# Rosendale Woodbank — Site Setup

## Goal

Create a single-page static website for the Rosendale Woodbank, a community firewood program. The site is informational only — no forms, no JavaScript, no framework. Just one `index.html` file with inline CSS, deployed to GitHub Pages.

## Reference

`reference/rosendale-woodbank.tsx` contains the current version of this page, written as a React Native / Expo component. Use it as the source of truth for **all content, structure, colors, and layout**. Convert it faithfully to plain HTML and CSS. Do not change the copy, do not add features, do not rearrange sections.

## Technical Requirements

- **Single file:** `index.html` at the repo root. All CSS inline in a `<style>` tag. No external dependencies.
- **Responsive:** One breakpoint at `600px`. Below that, reduce hero title from 42px to 32px, hero subtitle from 20px to 17px, and content horizontal padding from 32px to 20px. Use a `@media` query.
- **Favicon:** Emoji favicon using an inline SVG data URI (same technique as the reference file).
- **Page title:** "Rosendale Woodbank"
- **Font stack:** Use a clean system font stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif`
- **No JavaScript.** The page is fully static content.

## Color Palette (from reference)

| Token           | Value                        |
|-----------------|------------------------------|
| heroBackground  | `#2d4a3e`                    |
| heroText        | `#f5f1eb`                    |
| pageBackground  | `#faf7f2`                    |
| heading         | `#2d4a3e`                    |
| body            | `#3b3330`                    |
| cardBackground  | `#f0ebe4`                    |
| cardBorder      | `#d6cfc4`                    |
| ctaBackground   | `#2d4a3e`                    |
| ctaText         | `#f5f1eb`                    |
| divider         | `rgba(245, 241, 235, 0.3)`  |
| footerText      | `#8a8078`                    |

## Page Structure

The page has these sections in order — all content is in the reference file:

1. **Hero** — dark green background, centered emoji (🪵), title, horizontal divider, italic subtitle
2. **The Problem** — body text about heating costs
3. **The Idea** — two paragraphs about woodbanks
4. **What We Have So Far** — current resources
5. **What We Need** — four cards, each with an emoji icon, bold title, and body text:
   - 📍 A Processing Site
   - 🤝 Volunteers
   - 🌳 Wood
   - 💬 Community Input
6. **How It Would (Wood) Work** — three paragraphs about operations
7. **Who Benefits** — community value
8. **Get Involved (CTA)** — dark green rounded box with email (`rosendale.woodbank@gmail.com`). Make the email a `mailto:` link.
9. **Footer** — light italic disclaimer text, separated by a top border

## Layout Notes

- Content area is max-width `720px`, centered.
- "Need" cards use a horizontal layout: emoji icon on the left, text on the right. On very narrow screens, this is fine to keep as-is (the cards are flexible enough).
- The CTA box has the email in a semi-transparent white pill (`rgba(255,255,255,0.12)` background, `8px` border-radius).
- The hero divider is a small centered bar: `48px` wide, `2px` tall, semi-transparent.

## Deployment

Set up GitHub Pages to serve from the root of the `main` branch. That's it — just `index.html` at the root.

## What NOT to do

- No JavaScript
- No build tools, no npm, no frameworks
- No extra files (no CSS file, no images, no fonts)
- Don't change the copy or section order from the reference
- Don't add analytics, tracking, cookie banners, or anything else
- Don't over-engineer this — it's a community proposal page, not a web app
