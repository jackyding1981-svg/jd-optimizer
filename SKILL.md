---
name: jd-optimizer
description: Analyzes and rewrites job descriptions (JDs) based on market trends and best practices. Use this skill when a user uploads a JD and asks to analyze, optimize, rewrite, or enhance it.
---

# JD Optimizer Skill

This skill guides the process of transforming a traditional job description (JD) into a modern, effective, and data-driven one. It follows a three-step workflow inspired by the principles of deconstruction, reconstruction, and market analysis.

## Workflow Overview

1.  **Deconstruct & Analyze**: Systematically parse the user-provided JD and assess its quality.
2.  **Research Market Trends**: Analyze the broader job market for the same role to identify best practices and emerging requirements.
3.  **Reconstruct & Optimize**: Synthesize findings to generate a new, high-quality JD.

---

## Step 1: Deconstruct & Analyze the Original JD

Your first task is to perform a deep analysis of the original JD provided by the user.

### 1.1. Read the Analysis Framework

Before you begin, you MUST read the analysis framework to understand the required dimensions and quality criteria.

```bash
cat /home/ubuntu/skills/jd-optimizer/references/jd-analysis-framework.md
```

### 1.2. Extract Structural Information

Read the user's JD file. Based on the `Structural Dimensions` table in the framework, extract all available information. If a dimension is not present, mark it as "Not specified".

### 1.3. Score the JD's Quality

Using the `Quality Scoring Criteria` table, score the original JD on a scale of 1-5 for each criterion. Provide a brief justification for each score.

### 1.4. Generate the Analysis Report

Copy the analysis report template to a new file:

```bash
cp /home/ubuntu/skills/jd-optimizer/templates/jd-analysis-report.md ./jd_analysis_report.md
```

Fill in the `Structural Analysis` and `Quality Assessment` sections of `jd_analysis_report.md` with your findings from the previous steps. Also, list any `Common Issues` you identified.

---

## Step 2: Research Market Trends

Now, broaden your scope to understand how this role is positioned in the current job market.

### 2.1. Formulate Search Queries

Based on the standardized `job_title` from your analysis, create search queries to find similar job descriptions online. Use multiple query variations.

**Example Queries**:
- "Senior Data Analyst job description"
- "Data Analyst responsibilities and skills"
- "Top company Data Analyst JD examples"

### 2.2. Analyze Search Results

Use the `search` tool to execute your queries. Review at least 5-10 high-quality JDs from the search results. As you review, look for:

- **Trending Skills**: What new tools, technologies, or methodologies are frequently mentioned?
- **Common Responsibilities**: Are there common themes or outcomes that are missing from the original JD?
- **Best Practices**: Note effective structures, compelling language, and strong value propositions.

### 2.3. Update the Analysis Report

Synthesize your research findings and add them to the `Market Trend Insights` section of your `jd_analysis_report.md` file.

---

## Step 3: Reconstruct & Optimize the New JD

This is the final step where you create the new, optimized JD.

### 3.1. Read the Output Template

First, familiarize yourself with the structure and principles for the new JD.

```bash
cat /home/ubuntu/skills/jd-optimizer/references/jd-output-template.md
```

### 3.2. Synthesize and Write

Based on **all** your findings (original JD analysis + market research), write the new JD. Follow the structure and principles from the output template. Ensure the new JD:

- Addresses the weaknesses of the original JD.
- Incorporates market trends and best practices.
- Presents a clear and compelling value proposition.
- Is written in the same language as the original JD.

### 3.3. Final Delivery

Deliver two files to the user:

1.  `jd_analysis_report.md`: The completed analysis report.
2.  `optimized_jd.md`: The final, rewritten job description.

Present these as the result of the optimization process.
