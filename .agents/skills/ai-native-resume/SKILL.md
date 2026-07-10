---
name: ai-native-resume
description: Assist in modifying, tailoring, and managing the AI-native HTML resume for specific target positions.
---

# AI-Native Resume Customization Skill

This skill governs how the agent should structure, modify, and format the user's single-file HTML resume. The goal is to keep the resume highly professional, clean, print-ready, and tailored to specific job applications using clean variant management without duplicating files.

---

## 1. Core Principles

### Target Job Context (Mandatory First Step)
Before suggesting or making any edits, **always identify the company, industry, or specific position** the user is applying for. Every formatting, tone, and visibility decision must be aligned with this context.

### Variant Management (No Duplicate Files)
* Keep all variations of content (e.g., different styles of work experience descriptions, project variants) inside the **same HTML file**.
* Toggle content visibility using `class="hidden-section"` (which is styled as `display: none;`).
* Avoid rewriting bullet points each time the position changes. Instead, maintain separate predefined versions in the HTML code and update the visible section based on the target role.
* Maintain a "Resume Variant Guide" at the top of the HTML file (as comments) explaining the mapping of variants (e.g., `A = Research`, `B = Backend/Infra`, `C = ML Research`).

---

## 2. Structural & Layout Guidelines

### Section Ordering & Weighting
* **Projects vs. Experience**: If the candidate has more projects than job experience, or if the projects are significantly more relevant to the target job, place the **Technical Projects** section before the **Work Experience** section.
* Evaluate the relevance weight of projects and work experiences to determine the optimal ordering for the application.

### Visual Separation
* Ensure all parts/sections are clearly separated by visual dividers (e.g., horizontal lines, section borders, or distinct spacing).

### Section Headings
* **Do not use numbered prefixes** for sections (e.g., use `<h2>Education</h2>` instead of `<h2>1. Education</h2>` or `<h2>3. Technical Projects</h2>`). Remove any existing numbers to keep the layout modern and clean.

---

## 3. Section-Specific Rules

### Skills Classification
* For computer/technology-focused roles, categorize the skills cleanly. Example categories:
  - Programming Languages
  - Systems & Backend / Frameworks
  - Hardware & Edge Systems / Databases
  - Tools & Developer Utilities
* **Skill & Category Sequencing**:
  - **Category Sequencing**: Dynamically order the skill groups (e.g. placing "Hardware & Edge Systems" first for embedded roles, or "Programming Languages" first for general software roles).
  - **Individual Skill Prioritization**: Within each skill group, sort specific skills so that the most relevant ones to the target job appear first (e.g. placing "Swift" first for iOS roles, or "LLM Agents" first for AI application roles).

### Technical Projects
* **Remove years/dates** from the project entries. Focus purely on technical accomplishments and impact.
* Make sure project titles are clean and sub-headings match the target domain keywords.

---

## 4. PDF/Print Optimization (Aesthetics)
* Keep the styling clean and premium (e.g., Inter font, sleek dark text, subtle accents).
* Use CSS variables for easy personalization (e.g., modifying the accent color to match the target company's brand guidelines).
* Ensure margins and padding are structured such that the resume compiles perfectly to a single PDF page (or exactly two pages) without trailing overflow or orphaned headers.
* Include print-specific styles (e.g., `@media print`) if necessary to prevent layout breakage during PDF export.
* **Page-Break Spacing**: If adding manual `<br>` tags to push a section to the next page for layout matching, include 3–4 extra `<br>` tags (e.g. 5–6 total) to ensure the pushed section has a top margin and doesn't start compressed at the very top of the next page.

---

## 5. Formatting & Style Reference (CSS)

Any modifications, additions, or expansions to the resume HTML must strictly adhere to the established design system:

### Typography
* **Font Family**: `'Inter', -apple-system, sans-serif`
* **Line Height**: `1.6` (screen), `1.5` (print)

### Color Palette (CSS Variables)
* `--text-dark`: `#111827` (almost black; used for main headings and descriptions)
* `--text-light`: `#4b5563` (medium gray; used for locations, dates, and minor metadata)
* `--accent`: `#2563eb` (royal blue; used for hyperlinks, highlights, and subtle accents)
* `--border`: `#e5e7eb` (light gray)

### Component Layout Specifications
1. **Resume Container (`body`)**:
   * Max width: `850px`
   * Desktop padding: `40px`
   * Print padding: `20px 40px`
2. **Main Header (`header`)**:
   * Centered alignment.
   * `h1` (Name): `28px`, `font-weight: 700`, uppercase, letter-spacing `-0.025em`.
   * `.contact`: `13px` font-size, margin-top `10px`, color `--text-light`.
3. **Section Headings (`h2`)**:
   * Size: `15px`, `font-weight: 600`.
   * Uppercase, letter-spacing `0.05em`.
   * Border bottom: `2px solid var(--text-dark)`.
   * Padding bottom: `4px`.
   * Margins: margin-top `25px` (or `20px` in print), margin-bottom `12px` (or `8px` in print).
4. **General Entries (`.entry`)**:
   * Margin bottom: `16px` (or `12px` in print).
   * `.entry-header` (Company/Org name & timeline): `display: flex`, `justify-content: space-between`, baseline aligned, `font-weight: 600`, size `15px`.
   * `.entry-sub` (Title & Location): `display: flex`, `justify-content: space-between`, baseline aligned, italic, color `--text-light`, size `14px`, margin-bottom `4px`.
   * Bullet list (`ul`): `padding-left: 20px`, size `14px`, color `--text-dark`. Individual `li` elements have `margin-bottom: 4px`.
5. **Skill Blocks (`.skill-group`)**:
   * Margin-bottom: `8px`, size `14px`.
   * Labels (`.skill-label`): `font-weight: 600`, color `--text-dark`.
   * Additional bold indicators (`strong` tags): `font-weight: 600`.
