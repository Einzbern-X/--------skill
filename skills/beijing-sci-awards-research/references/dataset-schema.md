# Awards Dataset Schema (建议)

用于把“北京市科技奖项”调研结果做成结构化数据（便于后续筛选、对比、补全、年度更新）。

## 表 1：Award Programs（奖项/项目级）

| 字段 | 类型 | 说明 |
|---|---|---|
| award_program_name | string | 奖项名称（如：北京市科学技术奖） |
| award_program_alias | string | 常用别名/简称（如有） |
| level | enum | 市级/区级/行业协会/其他（默认：市级） |
| competent_authority | string | 主管单位 |
| organizer | string | 承办单位/组织单位（如有） |
| legal_basis_title | string | 政策/办法文件名 |
| legal_basis_doc_no | string | 文号（如有） |
| legal_basis_date | string | 发布日期（YYYY-MM-DD 或 YYYY-MM） |
| legal_basis_url | string | 官方来源链接 |
| categories | string | 奖项类别（概述） |
| grades | string | 等级/奖次（概述） |
| quota | string | 名额/数量（如有） |
| eligibility | string | 申报条件摘要 |
| process | string | 评审流程摘要 |
| timeline | string | 时间节点摘要（申报/评审/公示/授奖） |
| winners_entry | string | 历年获奖入口说明（公示/下载） |
| winners_url | string | 历年获奖入口链接（优先官方） |
| last_verified_at | string | 最后核验日期（YYYY-MM-DD） |
| notes | string | 备注 |

## 表 2：Award Cycles（年度/批次级，可选）

| 字段 | 类型 | 说明 |
|---|---|---|
| award_program_name | string | 对应表 1 |
| year | int | 年份 |
| call_title | string | 当年申报通知标题 |
| call_url | string | 申报通知链接（官方） |
| open_date | string | 申报开始 |
| close_date | string | 申报截止 |
| publicity_title | string | 公示标题 |
| publicity_url | string | 公示链接 |
| announcement_title | string | 授奖/通告标题 |
| announcement_url | string | 授奖/通告链接 |
| download_url | string | 名单/附件下载链接（如有） |
| last_verified_at | string | 最后核验日期 |

## 统一规范

- URL 必须可追溯到官方站点；第三方仅作为线索，notes 中标注。
- 日期字段尽量规范化；无法确定则使用 YYYY-MM 或留空。
