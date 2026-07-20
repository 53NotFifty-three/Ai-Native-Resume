---
name: ai-native-resume
description: Assist in analyzing target job positions, performing pre-edit evaluations, and tailoring the AI-native HTML resume for specific applications.
---

# AI-Native Resume Customization & Strategy Skill

This skill governs how the agent analyzes target position requirements, performs pre-edit evaluations, and tailors candidate experience for specific target applications.

---

## 1. Job Targeting & Pre-Edit Analysis Workflow

### Target Job Context (Mandatory First Step)
Before suggesting or making any edits, **always identify the company, industry, or specific position** the user is applying for. All tone and visibility decisions must align with this target role.

### Mandatory Pre-Edit Analysis (Artifact Generation)
Before modifying the resume for a new position, perform a deep analysis from two perspectives and save it as a markdown artifact (e.g., `pre_edit_analysis.md`):

#### 第一部分：招聘官视角（简历评估）
Evaluate the candidate's resume strictly against the target position requirements:
* **关键资格分析**：
  * **硬技能**：识别并列出与职位描述最匹配的关键技术、工具和专业知识。
  * **软技能**：评估领导力、解决问题能力、沟通与团队协作能力。
  * **经验匹配度**：分析工作经历与项目经验的相关度。
  * **加分项**：指出行业深度与独特优势。
* **综合评估与风险提示**：
  * **亮点总结**：总结候选人的突出竞争优势。
  * **潜在风险 (Red Flags)**：指出疑虑或需要警惕的信号。
  * **结论**：给出明确结论（如“完美匹配”）。

#### 第二部分：职业教练视角（个人品牌塑造）
1. **提炼个人品牌声明**：用一句话总结候选人的核心价值主张。
2. **打造标志性职业故事**：挖掘 2-3 个最能体现成就与解决问题能力的“标志性故事”。
3. **重塑劣势为优势**：将背景转换或跨界经历转化为适应性与学习能力的优势。
4. **撰写“为什么是我”核心叙述**：提供可直接用于 Cover Letter 或 LinkedIn 的精练文案。

---

## 2. Content Structuring & Value Framework

### Four-Value Categorization
When organizing or revising accomplishments for a target role, structure bullet points around four core values:
1. **Delivery**: Performing standard duties, ensuring pipelines run stably and as scheduled.
2. **Innovation**: Introducing creative methods or systems to improve performance and quality.
3. **Acceleration**: Bypassing time overhead and speeding up project timelines or workflows.
4. **Collaboration**: Translating complex technical/data results into digestible summaries for stakeholders.

### Scenario & Skill Context Integration
* **Contextual Framing**: Bullet points may describe the business scenario or challenge to provide background.
* **Skill Integration**: Explicitly highlight technical skills within descriptions using objective third-person phrasing (e.g., *"Leveraged knowledge in [Skill/Domain] to..."*).

---

## 3. Role-Relevance & Skill Classification

### Skills Classification & Ordering per Role
* **Category Sequencing**: Dynamically order skill groups according to target position priorities (e.g., place "Embedded & Hardware Systems" first for embedded roles, or "Programming Languages" first for general software roles).
* **Individual Skill Prioritization**: Within each skill group, list the most relevant skills first for the target role.
* **Role Relevance Filtering**: Omit skills that are completely irrelevant to the target role to maintain maximum scannability and impact.
