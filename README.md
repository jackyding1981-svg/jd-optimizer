# JD Optimizer

**AI-Powered Job Description Intelligent Reconstruction System**

JD Optimizer 是一个基于 AI Agent 的岗位描述（JD）智能优化技能，能够对传统 JD 进行系统分析、市场趋势研究，并生成优化后的新 JD。

## 核心功能

### 三步工作流

| 步骤 | 名称 | 核心动作 |
|------|------|---------|
| Step 1 | **解构与分析** | 对原始 JD 进行 16 个维度的结构化信息提取，并按 8 项质量标准评分（1-5分） |
| Step 2 | **市场趋势研究** | 在网络上搜索 5-10 份同类岗位的高质量 JD，分析热门技能、共性职责和最佳实践 |
| Step 3 | **智能重构** | 综合分析结果和市场洞察，按照现代 JD 模板重新撰写，生成分析报告和优化后的新 JD |

### 16 维分析框架

覆盖五大板块：**基本信息**（岗位名称、部门、汇报关系、工作地点）、**任职资格**（学历、经验年限、年龄、证书/资质）、**能力要求**（硬技能/技术栈、软技能、语言能力、胜任力模型）、**岗位内容**（核心职责、绩效指标）、**吸引力要素**（薪酬福利、发展路径）。

### 8 项质量评分标准

完整性、具体性、胜任力导向、包容性、雇主价值主张、市场对齐度、结构规范性、前瞻性。

## 文件结构

```
jd-optimizer/
├── SKILL.md                              # 核心指令文件
├── README.md                             # 项目说明
├── references/
│   ├── jd-analysis-framework.md          # 16 维分析框架 + 8 项评分标准
│   └── jd-output-template.md             # 优化 JD 输出模板
└── templates/
    └── jd-analysis-report.md             # 分析报告模板
```

## 部署与运行

### 环境要求

- Manus AI Agent 运行环境
- 已安装 `git`

### 部署步骤

1. **克隆仓库**：
   ```bash
   git clone https://github.com/jackyding1981-svg/jd-optimizer.git
   ```

2. **移动到技能目录**：
   将克隆的 `jd-optimizer` 文件夹移动到 Manus AI Agent 的技能目录（通常是 `/home/ubuntu/skills/`）。
   ```bash
   mv jd-optimizer /home/ubuntu/skills/
   ```

3. **验证安装**：
   在 Manus AI Agent 中，通过 `/skill-finder` 或类似命令检查 `jd-optimizer` 技能是否已被识别。

### 运行方式

1. **上传 JD 文件**：
   在 Manus AI Agent 的聊天界面中，上传一份您需要优化的传统 JD 文件（支持 PDF、Word、图片等格式）。

2. **触发技能**：
   在上传文件后，发送消息 `/jd-optimizer` 来手动触发技能。

3. **查看结果**：
   系统将自动执行三步工作流，并最终交付两个核心文件：
   - **JD 分析报告** (`jd-analysis-report.md`)：包含对原始 JD 的全面诊断和市场洞察。
   - **优化后的新 JD** (`optimized-jd.md`)：一份可以直接使用的、专业且现代化的新版 JD。

## 交付成果

- **分析报告**（Markdown 格式）：涵盖原始 JD 解构、质量评分雷达图、市场对标分析、优化建议
- **优化 JD**（Markdown 格式）：按照现代 JD 模板重新撰写的完整岗位描述

## 理论基础

本技能的设计参考了"基于生成式 AI 的岗位描述重构研究"的核心框架，融合了 NLP 岗位分析、技能知识图谱和生成式 AI 三大技术方向。

## License

MIT
