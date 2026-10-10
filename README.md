# 📈 stock-pretrade-checklist_Skill

股票投资下单前的自我反问与决策自检防风墙 🛡️

## 🚀 Description

This repository, `stock-pretrade-checklist_Skill`, aims to provide a system for self-reflection and decision-making checks before executing stock trades. It acts as a protective wall against impulsive decisions, ensuring investors go through a rigorous review process. The project contains a variety of Markdown files detailing checklists, templates, and references for various trading strategies and risk disciplines, alongside a Python script for potential utility or example purposes.

## 📚 Table of Contents

- [Project Title & Badges](#project-title--badges)
- [Description](#description)
- [Table of Contents](#table-of-contents)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [How to Use](#how-to-use)
- [Project Structure](#project-structure)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Important links](#important-links)
- [Footer](#footer)

## ✨ Features

- **Pre-Trade Decision Support:** Provides tools and frameworks to aid in making informed trading decisions.
- **Risk Management Focus:** Emphasizes self-reflection and risk discipline before executing trades.
- **Strategy Checklists:** Offers detailed checklists for various trading strategies like trend-following, value investing, and short-term thematic plays.
- **Template System:** Includes templates for decision summaries, trade cards, and self-check reports.
- **Reference Materials:** Contains API references and core risk discipline guidelines.
- **Example Script:** A placeholder Python script (`example.py`) suggests potential for utility functions or automation within the skill.

## ✨核心设计
- **按风格裁剪组合：** C 模块每次必读；价值长线加载 V，趋势波段加载 T（V 仅取治理 / 泡沫红线排雷），短线题材加载 H+T，矩阵已写死在 SKILL.md。
- **按品种裁剪：** 个股走全套；ETF 换为指数估值分位 / 折溢价 / 跟踪误差；可转债换为债底 / 溢价率 / 强赎条款；未覆盖的专项阈值不臆造，标注 "待用户补充口径"。
- **一票否决机制：** 每个模块末尾有编号红线（C-R1…、V-R1…、T-R1…、H-R1…），命中即终止并判 🔴；"不知道 / 听消息 / 凭感觉" 一律不放行；情绪测温不过直接熔断。
- **量化卡口强制现算：** 单笔风险、盈亏比、仓位、回撤回本涨幅均要求用计算器核算，不接受口算。
- 四份资料的数字阈值（0.5%–1%、20%、1:3、50% 质押率、A 股费率、茅台 / 美的标杆数据等）均原样保留，每份模块标注了来源作者。

## 🛠️ Tech Stack

- **Languages:** Python, Markdown, Text
- **Frameworks:** Python

## ⬇️ Installation

This project primarily consists of documentation and a single example Python script. There are no explicit dependencies or build processes indicated in the provided analysis.

To run the example Python script:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/YyyyyyoungC/stock-pretrade-checklist_Skill.git
    cd stock-pretrade-checklist_Skill
    ```
2.  **Navigate to the scripts directory:**
    ```bash
    cd Skill_stock-pretrade-checklist/scripts/
    ```
3.  **Execute the example script:**
    ```bash
    python example.py
    ```

**Note:** The `example.py` script is a placeholder and currently does not perform any complex operations. You may need to add Python environment setup if you intend to expand its functionality.

## 💡 Usage

The primary use case for this project is to serve as a comprehensive guide and decision-making framework for stock investors before they place a trade. It encourages a disciplined approach by prompting investors with critical questions and checks.

**Real-world use cases:**

- **Daily Trading Routine:** Investors can consult the relevant checklists (e.g., `trend-buy-checklist.md`, `theme-sentiment-checklist.md`) each morning before the market opens to align their trading plan.
- **Investment Decision Validation:** Before committing capital to a specific stock, users can use templates like `decision-onepager-template.md` to document their rationale and self-assess risks.
- **Risk Mitigation:** Referencing `core-risk-discipline.md` and `investment-pitfalls-checklist.md` can help investors avoid common mistakes and manage their risk exposure effectively.
- **Skill Development:** The extensive documentation within the `自检Skill原始知识库文档` folder can be used for personal learning and improvement in trading methodologies.

## 🔧 How to Use

1.  **Review Documentation:** Familiarize yourself with the various Markdown files located in the `Skill_stock-pretrade-checklist/` and `自检Skill原始知识库文档/` directories. These documents outline strategies, checklists, and self-assessment prompts.
2.  **Utilize Templates:** When considering a trade, use the provided templates (e.g., `trade-card-template.md`, `selfcheck-report-template.md`) to structure your analysis and decision-making process.
3.  **Follow Checklists:** For specific trading styles (e.g., trend following, value investing), use the corresponding checklists (e.g., `trend-buy-checklist.md`, `value-long-checklist.md`) to ensure all critical factors have been considered.
4.  **Consult References:** Refer to `api_reference.md` for any technical details or `core-risk-discipline.md` for fundamental risk management principles.
5.  **Run Example Script (Optional):** If you plan to extend the functionality, you can use `Skill_stock-pretrade-checklist/scripts/example.py` as a starting point. Modify it to automate parts of your pre-trade checklist process.

## 📂 Project Structure

```plaintext
stock-pretrade-checklist_Skill/
├── README.md
└── Skill_stock-pretrade-checklist/
    ├── SKILL.md                                  主控：CRO角色、风格裁剪矩阵、7步自检流程、8条交互铁律、三档裁决
    ├── assets/
    │   ├── decision-onepager-template.md         12问决策一页纸 + 落签承诺协议（V 风格）
    │   ├── example_asset.txt
    │   ├── selfcheck-report-template.md          自检结论单（三态结果+红线+待补证据+量化核算+裁决）
    │   └── trade-card-template.md                单笔交易卡片（T/H 风格通过后填写，盘前冻结）
    ├── references/
    │   ├── api_reference.md
    │   ├── core-risk-discipline.md               【C·每次必读】闲钱检查、风险预算(单笔≤1%/单股≤20%)、
    │   │                                          A股交易成本与T+1卡点、三重止损三类出场、六大偏差、
    │   │                                          情绪体温计熔断、七步落地、三禁令三复盘、12问落签、7条红线
    │   ├── theme-sentiment-checklist.md          【H·短线题材】逻辑/资金/梯队三问、七类催化、
    │                                              一日游5信号、爆发当日六步、5条红线
    │   ├── trend-buy-checklist.md                【T·趋势波段】趋势/位置/盈亏比(≥1:3)/确认信号四要素、
    │   │                                          三类买点、四个不能买位置、买入前七问、卖点、5条红线
    │   └── value-long-checklist.md               【V·价值长线】能力圈、现金流/杜邦ROE/护城河/治理红线、
    │   │                                          PE周期陷阱/DCF/SOTP、隐含预期、三情景压力测试、小A避坑速查、8条红线
    └── scripts/
        └── example.py
└── 自检Skill原始知识库文档/
    ├── 投资前自我反问与决策自检清单.md
    ├── 投资避坑清单【A】.md
    ├── 短线题材判断【pytime】.md
    └── 交易买点方法论【pytime】.md
```

## 📖 API Reference

An API reference file `Skill_stock-pretrade-checklist/references/api_reference.md` is present. However, its content is not detailed in the provided analysis. It likely contains information related to any programmatic interfaces or data structures relevant to the skill.

## 🤝 Contributing

Contributions are welcome! As this project is primarily documentation and a sample script, contributions could include:

- **Adding more detailed checklists or strategies.**
- **Improving the existing documentation.**
- **Developing the `example.py` script into a functional tool.**
- **Suggesting enhancements or new features.**

Please refer to the standard contribution guidelines for GitHub projects. Feel free to open an issue or submit a pull request.

## 📜 License

This project does not appear to have a specified license. Please consult the repository owner for licensing details.

## 🔗 Important links

- **Repository URL:** [https://github.com/YyyyyyoungC/stock-pretrade-checklist_Skill](https://github.com/YyyyyyoungC/stock-pretrade-checklist_Skill)

## 📝 Footer

---

© 2023 YyyyyyoungC. All rights reserved.

This project is maintained by YyyyyyoungC.

- **Repository:** [stock-pretrade-checklist_Skill](https://github.com/YyyyyyoungC/stock-pretrade-checklist_Skill)
- **Author:** [YyyyyyoungC](https://github.com/YyyyyyoungC)
- **Contact:** (Contact information not provided)

If you find this project helpful, please consider giving it a ⭐ Star, opening an 💡 Issue, or forking the repository! 🙏


---
**<p align="center">Generated by [ReadmeCodeGen](https://www.readmecodegen.com/)</p>**
