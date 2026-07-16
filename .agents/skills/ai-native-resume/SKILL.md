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

### Mandatory Pre-Edit Analysis (Artifact Generation)
Before starting any new resume modification or targeting a new position, the agent must perform a deep analysis from two perspectives and save it as a markdown file (e.g. `pre_edit_analysis.md`) in the artifacts directory:

#### 第一部分：招聘官视角（简历评估）
As a hiring manager with 20+ years of experience in the target industry, strictly evaluate the candidate's resume against the target position requirements:
* **关键资格分析**：
  * **硬技能**：识别并列出简历中与职位描述最匹配的关键技术、工具和专业知识。
  * **软技能**：评估简历中体现出的领导力、解决问题能力、沟通 and 团队协作能力。
  * **经验匹配度**：分析其工作经历与项目经验是否与岗位要求高度相关。
  * **加分项**：指出行业认证、专业领域的深度以及对候选人独特优势的塑造。
* **综合评估与风险提示**：
  * **亮点总结**：总结是什么让这位候选人脱颖而出。
  * **潜在风险 (Red Flags)**：指出简历中可能存在的疑虑或需要警惕的信号。
  * **结论**：给出明确的评估结论——是“优秀”，还是“完美匹配”？

#### 第二部分：职业教练视角（个人品牌塑造）
As a strategic career coach, provide personalized guidance based on the candidate's profile and target role:
1. **提炼个人品牌声明**：用一句话总结候选人的核心价值主张，清晰地传达出“我是谁”以及“我能带来什么”。
2. **打造标志性职业故事**：
  * 从简历中挖掘 2-3 个最能体现其成就、解决问题能力或独特优势的“标志性故事”。
  * 指导候选人如何在面试或社交场合中生动地讲述这些故事。
3. **重塑“劣势”为“优势”**：
  * 如果简历中存在职业中断、频繁跳槽或非传统背景等情况，请提供具体的语言和叙事策略，将其重塑为适应性、学习能力或跨界优势的证明。
4. **撰写“为什么是我”的核心叙述**：
  * 提供一段可以直接用于求职信、领英（LinkedIn）个人简介或自我介绍的精炼文案。这段话需要将候选人的经历、技能和热情与目标岗位的需求完美结合，建立情感共鸣。

### Variant Management (Master Template & Role-Specific Outputs)
* **Master Template File (`Liu_Hengzhi_Resume.html`)**: Serves as the single source of truth containing all candidate information. All position variants (e.g. Variant A = SWE, Variant B = AI Infra, Variant C = Backend) must coexist inside this file, organized and toggled using `class="hidden-section"`.
* **Role-Specific Output Files**: For target position applications, separate clean HTML files (e.g., `Liu_Hengzhi_Resume_SWE.html`, `Liu_Hengzhi_Resume_AI_Infra.html`, `Liu_Hengzhi_Resume_Backend.html`) must be generated from the master template.
* **Content Extraction**: In the role-specific output files, keep **only** the active content block for that role, and strip away all hidden section wrappers, other variants' blocks, and comments to produce a clean, lightweight, single-purpose resume file.

---

## 2. Content & Writing Guidelines (HR-Friendly)

### Plain Language ("写人话")
* Write in a way that is easily understood by non-technical recruiters or HRs who do not have a biology or highly niche technical background.
* Avoid heavy academic jargon; rephrase raw biological experiments (like cell cultures, microfluidics) to focus on engineering execution, project coordination, data integrity, and pipeline optimization.

### Four-Value Categorization
When drafting or revising accomplishments, organize them around these four core values:
1.  **Delivery**: Performing standard duties, ensuring project/pipeline runs stably and as scheduled.
2.  **Innovation**: Introducing creative methods or systems to improve performance and quality.
3.  **Acceleration**: Bypassing time overhead and speeding up project timelines or workflows.
4.  **Collaboration**: Facilitating communication, translating complex datasets into digestible summaries for stakeholders, and maintaining team/partner relations.

### Impact-Oriented Phrasing
* Always write bullet points starting with the impact/result (verb-first) followed by the action.
* **Example**: Use *"Reduced Z workflow turnaround time by building X data analysis pipeline and restructuring Y channel"* instead of *"Built X data analysis pipeline and restructured Y channel, reducing Z workflow turnaround time"*.

### Scenario & Skill Context (业务场景与技能融入)
* **Describe Business Scenarios**: Bullet points in experiences and projects must not only state what was done, but must specify the business scenario or context under which the work was performed.
* **Explicit Skill Integration**: Explicitly highlight the skills used in the experiences and projects.
* **Standard Phrasing**: Utilize the specific phrase `"Leveraged knowledge in [Skill/Domain] to..."` to introduce these skill applications.

### Truthfulness & Accuracy (No Hallucinations)
* **Never add skills or tools** that the candidate has not explicitly mentioned or used in their original/approved content. Avoid fabricating technologies.
* **Strictly follow the user's provided information** when rewriting bullet points. Do not invent project statistics, percentages, or achievements.
* **Avoid absolute quantitative claims** (e.g., '100% test consistency', '100% uptime') unless explicitly specified or backed by the candidate's original text (e.g., 'improved speed by 20%'). Use qualitative terms like 'high consistency', 'continuous operations', or 'minimized downtime' instead.
* **Post-Modification Check**: After updating the resume, perform a strict quality check to verify that all revised points map 1-to-1 with facts in the source materials and contain no hallucinations.

---

## 3. Structural & Layout Guidelines

### Section Ordering & Weighting
* **Projects vs. Experience**: If the candidate has more projects than job experience, or if the projects are significantly more relevant to the target job, place the **Technical Projects** section before the **Work Experience** section.
* Evaluate the relevance weight of projects and work experiences to determine the optimal ordering for the application.

### Visual Separation
* Ensure all parts/sections are clearly separated by visual dividers (e.g., horizontal lines, section borders, or distinct spacing).

### Section Headings
* **Do not use numbered prefixes** for sections (e.g., use `<h2>Education</h2>` instead of `<h2>1. Education</h2>` or `<h2>3. Technical Projects</h2>`). Remove any existing numbers to keep the layout modern and clean.

---

## 4. Section-Specific Rules

### Skills Classification
* For computer/technology-focused roles, categorize the skills cleanly. Example categories:
  - Programming Languages
  - Systems & Backend / Frameworks
  - Hardware & Edge Systems / Databases
  - Tools & Developer Utilities
* **Skill & Category Sequencing**:
  - **Category Sequencing**: Dynamically order the skill groups (e.g. placing "Hardware & Edge Systems" first for embedded roles, or "Programming Languages" first for general software roles).
  - **Individual Skill Prioritization**: Within each skill group, sort specific skills so that the most relevant ones to the target job appear first (e.g. placing "Swift" first for iOS roles, or "LLM Agents" first for AI application roles).
* **Proficient vs. Familiar Separation**:
  - Clearly separate skills by proficiency level (e.g., proficient vs. familiar/basic) within each skill group.
  - Follow the format: `<Category>: (Proficient) skill1, skill2, (Familiar) skill3, skill4`.
  - Example: `Programming Languages: (Proficient) Python, SQL, (Familiar) Java, C++`.

### Technical Projects
* **Remove years/dates** from the project entries. Focus purely on technical accomplishments and impact.
* Make sure project titles are clean and sub-headings match the target domain keywords.

---

## 5. PDF/Print Optimization (Aesthetics)
* Keep the styling clean and premium (e.g., Inter font, sleek dark text, subtle accents).
* Use CSS variables for easy personalization (e.g., modifying the accent color to match the target company's brand guidelines).
* Ensure margins and padding are structured such that the resume compiles perfectly to a single PDF page (or exactly two pages) without trailing overflow or orphaned headers.
* Include print-specific styles (e.g., `@media print`) if necessary to prevent layout breakage during PDF export.
* **Page-Break Spacing**: If adding manual `<br>` tags to push a section to the next page for layout matching, include 3–4 extra `<br>` tags (e.g. 5–6 total) to ensure the pushed section has a top margin and doesn't start compressed at the very top of the next page.

---

## 6. Formatting & Style Reference (CSS)

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
