# Company Intelligence for Job Search · 求职公司情报

Two standalone Agent Skills / 两套独立可调用的 Agent Skills（V1.1）。

| Language / 语言 | Skill |
|---|---|
| 中文 | [skills/zh/SKILL.md](skills/zh/SKILL.md) |
| English | [skills/en/SKILL.md](skills/en/SKILL.md) |

## Purpose / 功能
Identify the correct company, then report primary and secondary business lines, five recent reported fiscal years of consolidated revenue, major products and brands, headquarters country, and employee headcount and investments in a **user-selected region**.

准确识别公司，提供主营与次要业务线、最近五个已披露财年的合并总营收、产品品牌、总部国家，以及**用户指定地区**的员工人数与投资情况。

## Region / 地区
Country, state/province, city or clearly defined economic area. Default: **mainland China** when omitted. 用户可填写国家、省州、城市或明确经济区域；未填写时默认**中国大陆**。

## Examples / 示例
- `西门子` → 中文报告，默认中国大陆
- `西门子，目标地区：德国` → 中文报告，德国员工及投资
- `Siemens, region: United States` → English report, US employees and investments

## Reliability / 可靠性
Disambiguate names before reporting. Cite dated primary sources; distinguish consolidated from regional revenue, parent from subsidiary, realized from planned investment, and registered capital from actual investment. Explicitly label missing, estimated, conflicting or unverified data.

先消歧，后报告。引用注明日期的原始来源；区分集团与地区收入、母子公司、已完成与计划投资、注册资本与实际投资。未披露、估算、冲突、无法核实的信息必须明确标注。

## Install / 安装
Copy either `skills/zh` or `skills/en` into an Agent Skills-compatible skill directory. Both folders contain standalone `SKILL.md` files and may coexist.

Requires a browsing-capable agent for fresh research. This repository is a research instruction skill, not a live-data API.
