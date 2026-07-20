---
name: resume-format-style
description: HTML/CSS design system, layout specifications, typography, and PDF print formatting guidelines for resumes.
---

# Resume Format & Style Design System

This skill defines the technical formatting, CSS design system, HTML structure specifications, and PDF print layout guidelines for single-file HTML resumes.

---

## 1. Core Visual Specifications & Design Tokens

### Typography
* **Font Family**: `'Inter', -apple-system, sans-serif`
* **Line Height**: `1.6` (screen view), `1.5` (print view)

### Color Palette (CSS Variables)
* `--text-dark`: `#111827` (almost black; used for main headings and descriptions)
* `--text-light`: `#4b5563` (medium gray; used for locations, dates, and minor metadata)
* `--accent`: `#2563eb` (royal blue; used for hyperlinks, highlights, and subtle accents)
* `--border`: `#e5e7eb` (light gray)

---

## 2. Component Layout Specifications

1. **Resume Container (`body`)**:
   * Max width: `600px`
   * Desktop padding: `40px`
   * Print padding: `20px 40px`

2. **Main Header (`header`)**:
   * Centered alignment (`text-align: center`).
   * `h1` (Name): `28px`, `font-weight: 700`, uppercase, letter-spacing `-0.025em`.
   * `.contact`: `13px` font-size, margin-top `10px`, color `--text-light`.

3. **Section Headings (`h2`)**:
   * Size: `15px`, `font-weight: 600`.
   * Uppercase, letter-spacing `0.05em`.
   * Border bottom: `2px solid var(--text-dark)`.
   * Padding bottom: `4px`.
   * Margins: margin-top `25px` (or `20px` in print), margin-bottom `12px` (or `8px` in print).
   * **No numbered prefixes**: Use clean titles like `<h2>Education</h2>`.

4. **General Entries (`.entry`)**:
   * Margin bottom: `16px` (or `12px` in print).
   * `.entry-header` (Company/Org name & timeline): `display: flex`, `justify-content: space-between`, baseline aligned, `font-weight: 600`, size `15px`.
   * `.entry-sub` (Title & Location): `display: flex`, `justify-content: space-between`, baseline aligned, italic, color `--text-light`, size `14px`, margin-bottom `4px`.
   * Bullet list (`ul`): `padding-left: 20px`, size `14px`, color `--text-dark`. Individual `li` elements have `margin-bottom: 4px`.

5. **Skill Blocks (`.skill-group`)**:
   * Margin-bottom: `8px`, size `14px`.
   * Labels (`.skill-label`): `font-weight: 600`, color `--text-dark`.

---

## 3. Structural & Layout Rules

### Section Ordering & Weighting
* Evaluate the relevance weight of projects and work experiences to determine optimal section order for the target role.
* If technical projects are more relevant, place **Technical Projects** before **Work Experience**.

### Project & Timeline Formatting
* **Project Dates**: Include completion or development years aligned to the right in `.entry-header`.

---

## 4. PDF & Print Optimization

* **Single/Double Page Fit**: Ensure margins and padding allow the resume to compile cleanly to 1 or 2 PDF pages without orphaned headers or trailing overflow lines.
* **Print Styles**: Use `@media print` rules to optimize font sizes and line heights for printing.
* **Page-Break Spacing**: If manual `<br>` tags are needed to push a section cleanly to the next page, include 3–4 extra `<br>` tags (5–6 total) to prevent top-margin compression on the next page.
