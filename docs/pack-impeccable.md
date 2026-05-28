# pack-impeccable

### 📦 [pbakaus/impeccable](https://github.com/pbakaus/impeccable)

  - **介绍**：一个面向生产级前端界面的 UI 设计质量管理套件。它把设计上下文、设计系统、视觉生成、UX 审查、技术审计、打磨、响应式、动效、文案、性能和浏览器内视觉迭代放进同一个 `impeccable` skill 里。
  - **场景**：当你不只是想“做一个页面”，而是想让 AI 生成或改造的界面有明确设计判断、稳定设计上下文、可审查的质量门槛，并持续摆脱常见 AI UI 套板感时。
  - **组合**：早期可用 `frontend-design` 生成界面或组件，再用 `impeccable` 的 `shape` / `critique` / `audit` / `polish` 做质量闭环；如果只需要轻量规范核查，可配 `web-design-guidelines`。
  - **补充**：它对项目上下文很敏感，默认会读取 `PRODUCT.md` 和 `DESIGN.md`；缺失时优先用 `teach` / `document` 建立上下文。它还区分 `brand` 和 `product` 两种设计 register，避免所有界面都落进同一种审美模板。

---

## 建立设计上下文

- **`impeccable teach`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：引导建立或刷新项目的 `PRODUCT.md` 和 `DESIGN.md`，让后续 UI 工作有产品、用户、品牌、语气和设计原则可依赖。
    - **场景**：项目还没有稳定设计上下文，或者现有上下文太空、太旧、无法指导界面生成时。

- **`impeccable document`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：从现有项目代码和界面资产中提炼设计语言，生成或更新 `DESIGN.md`。
    - **场景**：已经有可用界面，希望把颜色、字体、组件、空间、动效等规则沉淀成后续可复用的设计文档时。

- **`impeccable extract`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：把页面里的可复用 token、组件和模式抽取到设计系统中。
    - **场景**：界面已经开始重复出现颜色、间距、按钮、卡片、表单等模式，需要从局部实现升级成可维护设计系统时。

---

## 生成与规划

- **`impeccable shape`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：在写代码前先做 UX/UI 方案规划，明确用户路径、信息层级、布局策略和视觉方向。
    - **场景**：功能还没动手实现，但你希望先把界面结构、交互状态和设计取舍想清楚时。

- **`impeccable craft`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：先 shape，再端到端实现一个 UI 功能或界面。
    - **场景**：要从需求直接推进到可运行的前端界面，并希望过程里带着设计判断，而不是只按功能堆组件时。
    - **组合**：适合承接 `teach` / `document` 建立的上下文，完成后再接 `critique`、`audit` 或 `polish`。

---

## 审查与质量门槛

- **`impeccable critique`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：做带启发式评分的 UX 设计评审，关注视觉层级、认知负荷、信息架构、一致性和可用性。
    - **场景**：界面已经存在，但你想知道它作为产品体验哪里不顺、哪里显得粗糙、哪里会让用户困惑时。

- **`impeccable audit`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：做技术质量审计，重点检查可访问性、性能、响应式表现和实现层面的 UI 风险。
    - **场景**：视觉方向大体可用，但准备交付前需要确认不同设备、浏览器、无障碍和性能没有明显坑时。

- **`impeccable polish`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：做发布前最后一轮质量打磨，把间距、层级、状态、文案、响应式和细节一致性拉到可交付水平。
    - **场景**：功能已经实现，剩下的问题不是“大改方向”，而是让页面从“能用”变成“可信、成熟、像真的产品”时。

---

## 强度与风格调节

- **`impeccable bolder`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：放大过于安全、平淡或模板化的界面，让视觉选择更明确、更有记忆点。
    - **场景**：页面没错但无聊，像默认 SaaS 模板或通用 AI 输出，需要更强品牌性或表达力时。

- **`impeccable quieter`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：压低过度吵闹、装饰太多或认知负荷过高的设计。
    - **场景**：界面元素都在抢注意力，视觉层级失控，或者产品型界面被做成了营销海报时。

- **`impeccable distill`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：移除不必要复杂度，把界面压缩到核心任务、核心信息和核心交互。
    - **场景**：页面功能太散、内容太多、层级太碎，需要回到最小但有力的体验结构时。

- **`impeccable delight`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：给界面加入克制但有记忆点的个性、微交互和情绪细节。
    - **场景**：基础体验已经稳，但希望产品更有性格，而不是只保持正确和中性时。

- **`impeccable overdrive`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：把视觉和交互推到更高表达强度，适合探索非常规、技术感或高冲击力的界面方向。
    - **场景**：品牌页、实验性页面、作品展示或主视觉需要突破常规，不满足于保守稳妥方案时。

---

## 视觉专项打磨

- **`impeccable colorize`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：为单调或灰度化界面加入有策略的色彩系统，而不是随意加强调色。
    - **场景**：界面信息结构还行，但颜色缺少角色、情绪或状态表达时。

- **`impeccable typeset`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：改善字体选择、字号层级、行长、字重和文本节奏。
    - **场景**：页面看起来“字很多但没层次”，标题、正文、标签、数字和说明文字之间缺少清晰关系时。

- **`impeccable layout`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：修正空间、对齐、节奏和视觉层级，让布局从机械排列变成有主次的界面结构。
    - **场景**：组件都在，但页面显得松散、拥挤、卡片化过度、对齐漂移或扫描路径不顺时。

- **`impeccable animate`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：加入有目的的动效和微交互，强调反馈、状态变化和空间关系。
    - **场景**：交互状态存在但缺少过渡、反馈或手感，或者动效太随意、太装饰化时。

---

## 产品体验修复

- **`impeccable harden`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：补齐生产级界面细节，包括错误状态、空状态、边界数据、国际化和异常路径。
    - **场景**：页面在理想数据下好看，但真实上线会遇到长文本、空数据、加载失败、权限限制、多语言等情况时。

- **`impeccable onboard`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：设计首次使用、空状态、激活路径和新用户引导。
    - **场景**：用户第一次进入产品不知道下一步做什么，或者空状态只是“暂无数据”而没有推动行动时。

- **`impeccable clarify`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：改善 UX 文案、标签、按钮、提示、错误信息和解释性文本。
    - **场景**：界面结构能用，但用词含糊、按钮不明确、错误提示不帮用户恢复，或者说明文字重复标题时。

- **`impeccable adapt`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：针对不同屏幕尺寸和设备形态调整界面。
    - **场景**：桌面端完成后需要补移动端、窄屏、宽屏、触控或不同断点的真实体验，而不只是简单堆叠时。

- **`impeccable optimize`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：诊断并修复 UI 性能问题，关注加载、渲染、交互响应和动画流畅度。
    - **场景**：界面视觉上完成了，但首屏、滚动、切换、动画或复杂组件让体验变慢时。

---

## 浏览器内迭代与快捷命令

- **`impeccable live`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：进入浏览器内视觉变体模式，选择页面元素并生成替代方案，适合边看边改。
    - **场景**：你需要对真实页面中的某个区域做多方案视觉迭代，而不是只在代码里抽象描述时。

- **`impeccable pin <command>`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：把 `impeccable` 的某个子命令固定成独立快捷命令。
    - **场景**：团队经常使用某个命令，比如 `polish` 或 `critique`，希望直接调用而不用每次写完整前缀时。

- **`impeccable unpin <command>`** ([pbakaus/impeccable](https://github.com/pbakaus/impeccable))
    - **介绍**：移除之前通过 `pin` 创建的快捷命令。
    - **场景**：某个快捷命令不再需要，或者团队想收回过多入口，保持命令表清爽时。
