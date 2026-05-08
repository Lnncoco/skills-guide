# 设计与体验

这一页集中放界面表达、交互体验、设计系统和终端体验相关的技能。

---

- **`frontend-skill` (艺术指导)** ([openai/skills](https://github.com/openai/skills))
    - **介绍**：偏视觉方向和首屏表现的前端设计 skill，强调界面要“像被设计过”，而不是只是把信息摆出来。
    - **场景**：你更在意页面气质、视觉冲击力和主画面完成度，而不是一般功能页面拼装时。
    - **补充**：**“海报而非文档。”** 拒绝 AI 生成的平庸卡片堆砌，强调首屏表现力和整体视觉层次。

- **`frontend-design` (前端落地)** ([anthropics/skills](https://github.com/anthropics/skills))
    - **介绍**：生成有鲜明美学方向、可直接落地、并且刻意避开通用 AI 套板感的前端界面实现。
    - **场景**：做 landing page、官网、dashboard、Web 组件，或者希望把现有前端做得更有辨识度时。
    - **组合**：如果还需要先定风格策略和体验方向，可先配 `ui-ux-pro-max`、`interaction-design`，最后再用 `web-design-guidelines` 审查实现。

- **`ui-ux-pro-max` (体验策略库)** ([nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill))
    - **介绍**：提供风格路线、配色、字体、布局、动画、组件体验和数据展示的系统化 UI/UX 建议。
    - **场景**：要选风格、定色板、调界面体验、评估视觉方向时。

## UX/UI 深度审查

- **`nielsen-heuristics-audit`** ([mastepanoski/claude-skills](https://github.com/mastepanoski/claude-skills))
    - **介绍**：按 Nielsen 启发式方法审查界面，集中识别可见性、反馈、一致性和容错性方面的典型问题。
    - **场景**：你已经有页面或组件实现，想从启发式可用性审查角度找出明显的 UX 坏味道时。
    - **补充**：更适合做结构化体验审查；如果问题更偏交互行为本身，可配合 `interaction-design` 一起看。

- **`interaction-design`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：聚焦交互行为本身，处理状态切换、反馈节奏、错误恢复、键盘鼠标路径和可访问性，而不是只谈视觉风格。
    - **场景**：设计组件行为、页面流程、loading / empty / error 状态，或者评估交互是否顺手时。

### 📦 [mindrally/skills](https://github.com/mindrally/skills)

- **`design-systems` (Token 治理)** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：将颜色、间距、排版等抽离为设计 token，强调一致性而不是随机生成的样式。
    - **场景**：页面越来越多，视觉规则开始漂移，需要把颜色、间距、字体和组件状态系统化时。

- **`css` (样式重构)** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：专注于现代 CSS 架构、变量、布局和可维护性。
    - **场景**：样式文件开始膨胀、冲突增多，或者你要整理布局和变量体系时。

### 📦 Stitch 自动化 ([google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills))

- **`design-md`** ([google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills))
    - **介绍**：从现有资产提炼语义化设计系统，输出 `DESIGN.md`。
    - **场景**：已经有页面或设计稿，希望抽出统一视觉语言供后续生成复用时。

- **`stitch-loop`** ([google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills))
    - **介绍**：基于设计规范开启多页面自动生成与集成循环。
    - **场景**：想让 Stitch 按固定设计语言持续推进多页面网站时。

- **`web-design-guidelines`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：按 Vercel 的界面规范审查 UI 代码和实现结果。
    - **场景**：要做 UI 评审、可访问性检查或界面规范核查时。

## TUI / 终端体验

- **`terminal-ui`** ([pproenca/dot-skills](https://github.com/pproenca/dot-skills))
    - **介绍**：专门处理终端界面的信息呈现、布局层次和交互反馈，兼顾可读性与终端内体验。
    - **场景**：你做的是终端里的结果页、信息面板或 TUI，希望它不只是“能看”而是信息组织更清楚、交互更顺手时。
