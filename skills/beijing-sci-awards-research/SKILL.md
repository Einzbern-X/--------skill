---
name: beijing-sci-awards-research
description: This skill should be used when the user asks to "research Beijing science and technology awards", "调研北京市科技奖项", "北京市科学技术奖", or discusses Beijing municipal science & technology awards policies and winners. Provides a structured research workflow and deliverables.
version: 1.0.0
---

# Beijing Science & Technology Awards Research

用于系统化调研「北京市科技奖项」（重点：北京市科学技术奖）并产出可复用的研究结论与材料清单。

## When to use

- 你要快速搞清楚北京市层面的科技奖项有哪些、由谁主管、评审/申报周期是什么
- 你要整理「北京市科学技术奖」的奖项设置、申报条件、评审流程、历年获奖信息入口
- 你要为领导/团队输出一份结构化调研报告（带引用来源、可追溯链接）

## Core workflow

### 1) Clarify scope

1. 明确调研对象：
   - 是否仅限「北京市科学技术奖」
   - 是否包含：区级奖项、行业协会奖、国家奖在京单位获奖（通常应排除）
2. 明确时间范围：近 1-3 年 / 近 5 年 / 全量
3. 明确输出形态：
   - 1 页要点总结
   - 详细报告（含表格）
   - 获奖项目/单位清单（结构化数据）

### 2) Build a source-of-truth list (prioritized)

优先级从高到低：

1. 北京市人民政府 / 市科委（或其现行机构名称）官方站点：政策、通知、申报指南
2. 权威媒体/政府公报：公示、通告
3. 第三方汇总（仅用于线索，不作最终依据）

要求：每条结论必须能回链到官方来源。

### 3) Extract key facts

对每个奖项（或对「北京市科学技术奖」的每个子项）提取字段：

- 名称（中英文如有）
- 主管/承办单位
- 法规/办法依据（文件名 + 发布日期 + 文号如有 + 链接）
- 奖项设置（类别/等级/名额/奖励方式）
- 申报条件（主体资格、成果要求、限制条款）
- 评审流程（阶段、材料、评审组织）
- 时间节点（申报期/公示期/授奖时间）
- 历年获奖信息入口（公示链接/名单下载）

### 4) Compile deliverables

输出三份材料（可按需删减）：

1. **Executive Summary**（要点）
2. **Research Report**（正文，含引用）
3. **Awards Dataset**（表格/CSV 字段建议见 `references/dataset-schema.md`）

### 5) Quality checks

- 结论是否都有官方链接支撑
- 链接是否可访问、是否需要登录
- 是否明确标注信息发布时间与适用年份
- 是否区分“政策规定”与“当年申报通知”的差异

## Suggested prompts

- “帮我调研北京市科学技术奖：奖项设置、申报条件、评审流程，并给出官方来源链接。”
- “整理近 5 年北京市科学技术奖获奖名单入口（公示/下载链接），并做一个字段化表格。”
- “对比北京市科学技术奖与国家科学技术奖：主管部门、奖项类别、申报条件差异（只引用官方来源）。”

## Notes

- 不要把第三方百科/自媒体当作最终依据；只能用来找线索。
- 如需抓取网页并抽取要点，优先使用内置网页抓取工具；必要时用浏览器验证。

## Related resources

- `references/dataset-schema.md`
- `references/search-queries.md`
- `references/report-outline.md`
