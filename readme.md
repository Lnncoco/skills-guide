# Skills Guide

当前技能总数：`70+` | 更新于：2026年5月

---

## 1. 软件工程与产品方法论 (Software & Product Methodologies)

本模块技能负责在“写下第一行代码”之前，解决“做什么”和“怎么做”的问题。

### 📦 [jwynia/agent-skills](https://github.com/jwynia/agent-skills)
- **`requirements-analysis` (需求诊断)**
    - **介绍**：它不是简单的文档生成器，而是一个**诊断工具**。它假设所有初始需求都是“假设”，核心目标是区分“用户想要的”和“用户底层的痛苦”。
    - **场景**：当你只有一个模糊想法（如“我想做个 SSG”）时，它会通过“问题考古”逼问你：谁在受苦？如果不做会怎样？
    - **行为**：它会强制产出 `Problem Statement Brief` 和 `Constraint Inventory`，在 `RA5` (Requirements Validated) 之前拒绝进入设计。
- **`system-design` (架构导航)**
    - **介绍**：专注于从需求到 `Walking Skeleton` 的转化。核心是 **Trade-offs** (权衡)。
    - **行为**：它会识别 `SD1` (Under-Engineering) 和 `SD2` (Over-Engineering)。如果你为只有 1 个用户的项目设计微服务，它会触发 `YAGNI` 审计。
    - **产出**：`Component Map`、数据流向图、以及最重要的 `Walking Skeleton` 定义——即系统最薄的端到端路径。
- **`architecture-decision` (关键决策)**
    - **介绍**：当面临 A 还是 B 的抉择（如：PostgreSQL vs MongoDB）时使用。
    - **逻辑**：基于“权衡三角形”（Simplicity, Flexibility, Performance）。没有完美的架构，只有最适合当前上下文的权衡。
    - **产出**：标准 `ADR` (Architecture Decision Record)。

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills) (压力测试)
- **`grill-me` (冷酷追问)**
    - **介绍**：Socratic (苏格拉底式) 访谈工具。它会针对你的方案进行 40-100 个问题的连续追问。
    - **行为**：它会沿着决策树的每一个分支向下走，直到所有模糊地带都被排干。它不仅提问，还会给出它推荐的答案供你参考。
- **`grill-with-docs` (约束压测)**
    - **介绍**：带上下文的 `grill-me`。它会检查你的方案是否违反了现有的 `CONTEXT.md` (领域模型) 或 `ADR`。
    - **场景**：在已有的大型项目中，确保新方案不背离已有的领域术语和历史决策。

### 📦 高级产品经理框架 (Product Management)
- **`product-manager-skills`** ([assimovt/productskills](https://github.com/assimovt/productskills))
    - **介绍**：包含 28+ 个高级产品经理工作流。融合了《The Mom Test》（妈咪测试）、《Shape Up》等顶级理论。
    - **行为**：强制进行 `problem-validation`（验证问题是否真实存在）、`scope-cutting`（无情地砍掉边缘需求），并输出真正可被技术团队执行的 `bet-sizing`（下注规模）文档。
- **`user-research-synthesis`** ([anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins))
    - **介绍**：专门用来处理海量、杂乱的用户访谈记录或工单反馈。
    - **行为**：提炼核心痛点，自动聚类成主题，并推导出现有产品的改进路线图。

### 📦 经典产品思维 ([wondelai/skills](https://github.com/wondelai/skills) 等)
- **`jobs-to-be-done`**
    - **介绍**：基于 Clayton Christensen 的 JTBD (焦布斯待办任务) 理论。引导 Agent 从“功能堆砌”转向“目标结果”。
    - **行为**：访谈识别客户“雇佣”产品的真实动机（功能、社交、情感），并输出规范的 Job Stories (When / I want / So I can)。
- **`domain-driven-design`**
    - **介绍**：基于 Eric Evans 的 DDD (领域驱动设计) 战术与战略模式。
    - **行为**：强制建立“通用语言”(Ubiquitous Language)，划定“有界上下文”(Bounded Contexts) 并设计“聚合根”(Aggregates)，防止系统退化为“大泥球”(Big Ball of Mud)。
- **`design-thinking`** ([melodic-software/design-thinking](https://github.com/melodic-software/design-thinking))
    - **介绍**：严格遵循斯坦福 d.school 的五步创新框架 (Empathize, Define, Ideate, Prototype, Test)。
    - **场景**：在产品极度早期、方向迷茫时，通过结构化的流程系统性地发掘创新切入点。
- **`senior-architect`** ([alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills))
    - **介绍**：一个自动化架构工具箱。提供 Python 脚本自动生成架构图、进行依赖分析。
    - **场景**：适合需要产出正式架构交付物或进行代码库依赖分析的场景。
- **`planning-with-files`** ([OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files))
    - **介绍**：Agent 的外部记忆系统。将思考过程持久化到 `task_plan.md` 等文件中。
    - **场景**：防止长任务在多轮对话后因 Context 限制而“失忆”。

---

## 2. 通用分析与哲学框架 (Cognitive & Philosophical Frameworks)

纯粹的分析问题、结构化表达和克服思维盲区的跨学科与哲学模型。这些模型不局限于写代码，可用于任何复杂的决策推演。

### 📦 商业逻辑与防盲从分析
- **`mckinsey-framework`** ([nicepkg/ai-workflow](https://github.com/nicepkg/ai-workflow))
    - **介绍**：将麦肯锡的咨询级方法论（如金字塔原理、问题树、SCQA）引入逻辑推演。
    - **行为**：在拆解复杂任务时，强制执行 **MECE 原则** (相互独立，完全穷尽)，确保方案无重叠、无遗漏，从而大幅节省大模型的 Context。
- **`six-thinking-hats`** ([neurofoo/agent-skills](https://github.com/neurofoo/agent-skills))
    - **介绍**：基于爱德华·德·波诺的“六顶思考帽”模型，用于克服 AI 的“盲目顺从性 (Agreeableness)”。
    - **行为**：在进行高风险决策前，强制 Agent 扮演 6 种独立角色进行顺序推演（比如黑帽专挑漏洞，黄帽专讲收益，绿帽专提备选方案），最后由蓝帽汇总。
- **`brainstorming`** ([obra/superpowers](https://github.com/obra/superpowers))
    - **介绍**：这是一个发散思维工具。
    - **场景**：目标明确但不确定具体实现路径，需要扩展思路时，用来探索 3-5 种候选方案。

### 📦 哲学与第一性原理 (Philosophical Models)
- **`socratic-questioning`** ([neurofoo/agent-skills](https://github.com/neurofoo/agent-skills))
    - **介绍**：苏格拉底式提问法。将 Agent 从“解答机”变为“辩证伙伴”。
    - **行为**：自动识别你指令中的隐藏假设，进行五层深度追问（澄清主张、探究证据、探索推论等），并生成反方辩论。
- **`first-principles-thinking`** ([swapnildahiphale/first-principles-thinking-skill](https://github.com/swapnildahiphale/first-principles-thinking-skill))
    - **介绍**：基于物理学和马斯克推崇的第一性原理。
    - **行为**：拒绝类比思维（“别人是怎么做的”），强制将复杂问题解构为最基础、不可辩驳的基石真理，然后从零开始推导创新方案。
- **`thinking-partner`** ([mattnowdev/thinking-partner](https://github.com/mattnowdev/thinking-partner))
    - **介绍**：内置 150+ 种跨学科的经典思维模型（包含二阶思维、奥卡姆剃刀、切斯特顿栅栏等）。
    - **行为**：将 Agent 转化为你的“智力陪练” (Sparring Partner)，专门负责挑战你的潜意识假设，暴露思维盲区。

---

## 3. 特定业务领域模型 (Domain-Specific Expertise)

垂直行业的专家级 Agent Skills，内置了该领域的专有逻辑、合规要求、数据接口甚至增长策略。

### 📦 增长与文案 (Growth & Copywriting)
- **`marketing-ideas`** ([coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills))
    - **介绍**：围绕 SaaS 和软件产品提供分门别类的增长、营销和推广策略库（包含 140+ 种经过验证的方法）。
- **`direct-response-copy`** ([weber-stephen/cursor-copywriting](https://github.com/weber-stephen/cursor-copywriting))
    - **介绍**：植入奥格威 (Ogilvy) 等广告大师的直接响应文案思维，拒绝 AI 默认的公文式乏味文案。
    - **行为**：强制使用 PAS 或 AIDA 框架，输出具有“钩子 (Hook)”属性、面向转化的真实文案。

### 📦 Web3 与区块链 (Web3 & Crypto)
- **`web3-agent-skills`** ([dAAAb/agent-skills](https://github.com/dAAAb/agent-skills))
    - **介绍**：涵盖 Web3 钱包、链上身份和去中心化 DApp 交互的专项模型。
- **`solidity-best-practices`** (社区最佳实践)
    - **介绍**：智能合约安全与 Gas 优化指南。
    - **行为**：极度强调安全。强制使用 CEI (Checks-Effects-Interactions) 模式防止重入攻击，并严格遵循 OpenZeppelin 的可升级代理合约标准 (UUPS/Diamond)。

---

## 4. 任务、Issue 与协作 (Matt Pocock 体系)

将庞大的架构方案拆解为可执行、可交付的颗粒度。

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)
- **`setup-matt-pocock-skills`**
    - **[底层配置]** 告知 Agent 你的 `Issue Tracker` (GitHub/Linear/Local) 和标签体系。**必须先运行此项。**
- **`to-prd` (PRD 合成)**
    - **介绍**：不做访谈，只做**合成**。基于当前上下文和代码库理解，自动生成包含 User Stories、Implementation Decisions 和 Testing Decisions 的完整 `PRD`。
- **`to-issues` (垂直切片拆解)**
    - **介绍**：将大任务拆成**最小可演示功能点**。
    - **拆解原则**：拒绝按层横向拆分（例如：先写数据库，再写 API），强制按功能**垂直切片**（例如：实现一个从 UI 到数据库都能走通的简单登录功能）。
    - **行为**：区分 `AFK` (Agent 可独立完成) 和 `HITL` (需要人介入决策) 任务。
- **`triage` (状态机管理)**
    - **介绍**：专业的 `Issue` 生命周期管理，确保每一个 `Issue` 都有明确的受理角色和状态。

---

## 5. 调试、测试与代码质量 (工程纪律)

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)
- **`diagnose` (硬核 Bug 诊断)**
    - **介绍**：6 阶段闭环。第 1 阶段 (Build a feedback loop) 占 90% 的努力。Agent 会尝试各种方式建立一个 2 秒内可运行的失败反馈（如快速脚本或单元测试）。
    - **行为**：**“没有反馈回路，就不准假设。”** 在看到 `Bug` 真正复现之前，Agent 会拒绝猜测原因。
- **`zoom-out` (高层建模)**
    - **场景**：当你面对几千行不熟悉的代码感到迷茫时。它会强制 Agent 停止看细节，先绘制模块地图和调用者关系图。
- **`tdd` (测试驱动开发)**
    - **行为**：**“先红后绿。”** 在写任何实现代码之前，必须先写一个能准确捕获目标行为失败的测试。
- **`improve-codebase-architecture` (代码深化)**
    - **介绍**：基于《A Philosophy of Software Design》。核心目标是**增加模块深度** (Deep Modules，即简单的接口背后隐藏复杂的行为)。
    - **行为**：识别“浅模块”(`Shallow Modules`，即接口和实现一样复杂的代码)，并提出重构建议。

### 📦 质量收束
- **`code-review`** ([google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli))
    - **介绍**：执行高信号的代码审查。不仅仅看代码风格，而是重点看逻辑 `Bug`、安全隐患和架构规则违反。
- **`clean-code`** ([AbsolutelySkilled/AbsolutelySkilled](https://github.com/AbsolutelySkilled/AbsolutelySkilled))
    - **介绍**：一套务实的 AI 代码准则。强制执行 `SRP` (单一职责) 和 `YAGNI`。
    - **行为**：内置“思考清单”，要求 Agent 在改动任何文件前先自问：谁依赖这个文件？修改会破坏什么？

---

## 6. 设计与体验

### 📦 [openai/skills](https://github.com/openai/skills)
- **`frontend-skill` (艺术指导)**
    - **行为**：**“海报而非文档。”** 拒绝 AI 生成的平庸卡片堆砌。强制执行硬规则——默认不使用卡片，Hero 必须全屏 (`Full-bleed`)，首屏如果拿掉背景图还能看，说明图选得太弱。
    - **产出**：具有高级感、呼吸感和明确视觉层次的界面。

### 📦 [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
- **`ui-ux-pro-max` (体验策略库)**
    - **介绍**：它是你的设计顾问。提供 50 多种风格 (Glassmorphism, Bento Grid 等) 和专业色板。
    - **场景**：当你需要为一个仪表盘定调子，或者需要一套专业的配色方案时。

### 📦 UX/UI 深度审查 (UX Auditing)
- **`uxui-evaluator`** ([uxuiprinciples/agent-skills](https://github.com/uxuiprinciples/agent-skills))
    - **介绍**：内置 168 项有学术研究背书的 UX 原则，以及 Nielsen 的 10 大可用性启发式评估。
    - **行为**：在生成前端代码前，或审查现有页面时，像资深 UX 架构师一样指出“体验坏味道 (UX Smells)”，如点击区域过小、层级视觉引导冲突等。

### 📦 [mindrally/skills](https://github.com/mindrally/skills)
- **`design-systems` (Token 治理)**: 将颜色、间距、排版抽离为 `Tokens`。确保 UI 的一致性而非随机生成的样式。
- **`css` (样式重构)**: 专注于现代 CSS 架构 (`Variables`, `Grid`, `Container Queries`)。

### 📦 Stitch 自动化 ([google-labs-code/stitch-skills](https://github.com/google-labs-code/stitch-skills))
- **`design-md`**: 从现有资产提炼语义化设计系统，输出 `DESIGN.md`。
- **`stitch-loop`**: 基于设计规范开启多页面自动生成与集成循环。

### 📦 UI 审查
- **`web-design-guidelines`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills)): 按 Vercel 标准审计 UI 代码的规范性与可访问性。

---

## 7. 语言、框架与工程生态 (Languages, Frameworks & Engineering)

涵盖从底层语言基础、UI 框架到构建工具及服务端架构的完整开发规范。为未来的 React, Go, Python 等全栈扩展预留了统一的归属地。

### 📦 JavaScript / TypeScript 与工程规范
涵盖 JS/TS 语言内功，以及大前端的包管理、构建与测试等工程化基建。
- **`javascript-mastery`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：深度讲解 33+ 个 JS 核心概念（闭包、事件循环、原型链等），提升底层理解。
- **`typescript-advanced-types`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：设计复杂泛型、条件类型及类型推导逻辑。应对高阶类型编程。
- **`antfu`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：Anthony Fu 的极简主义工程学。包括一整套完善的 `Lint`、格式化和多包 (`Monorepo`) 管理逻辑。
- **`pnpm`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：PNPM 的 Workspace、Catalog 及依赖治理最佳实践。
- **`vite`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：Vite 配置、插件开发与性能优化。
- **`unocss`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：UnoCSS 原子化样式的规则与预设配置。
- **`turborepo`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：Monorepo 任务图、缓存与边界配置。
- **`vitepress`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：基于 Vite 的现代文档站点构建规范。
- **`vitest`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：Vitest 单元测试与 Mock 最佳实践。
- **`tsdown`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：TypeScript npm 包的构建与发布规范。

### 📦 Vue 生态
- **`vue-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **行为**：**[默认开启]** 强制使用 `Composition API` + `<script setup>`。内置“组件拆分触发器”：当组件承担多于 1 个职责、有 3 个以上 UI 区域时，强制拆分。
- **`vue-debug-guides`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：专门处理难搞的响应式丢失、`SSR` 水合 (`Hydration`) 失败等 Vue 特有痛点。
- **`vue-pinia-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：侧重于 Store 的建模策略与响应式边界设计。
- **`vue-router-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：处理导航守卫、路由参数及组件生命周期的最佳模式。
- **`vue-testing-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：设计 Vitest 单测与 Playwright E2E 测试方案。
- **`create-adaptable-composable`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：教你编写接受 plain value, ref 或 getter 的库级 composable，强调 MaybeRef 兼容性。
- **`vue-jsx-best-practices`** & **`vue-options-api-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **场景**：应对特定语法要求和历史项目的兼容指南。

### 📦 React / Next.js 生态
- **`react-best-practices`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：Vercel 官方发布的 React 性能与架构指南。
    - **行为**：强制消除 Async Waterfalls (异步瀑布流)，使用并行数据获取；严禁乱用 Barrel Files (聚合导出文件) 以优化构建体积；强制在 Server Actions 内部进行鉴权。
- **`nextjs-app-router`** (社区最佳实践)
    - **介绍**：针对 Next.js App Router 模式的边界划分。
    - **行为**：严格控制 `use client` 与 `use server` 边界，提倡 React Server Components (RSC) 优先。

### 📦 Node.js 服务端生态
- **`backend-dev-guidelines`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：强制执行 **Routes -> Controllers -> Services -> Repositories** 的分层架构。这种结构对保障 Agent 的代码导航和长期维护至关重要。
- **`nodejs-best-practices`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：关于 Node 框架选型、异步流控、错误处理、以及生产环境安全的深度指南。

### 📦 Go 生态
- **`go-best-practices`** ([samber/cc-skills-golang](https://github.com/samber/cc-skills-golang))
    - **介绍**：Golang 综合最佳实践。覆盖并发 (Concurrency)、错误处理 (`fmt.Errorf("%w")`)、表驱动测试及 `context.Context` 传播。
    - **行为**：倡导“Type-First Development” (类型驱动开发) 和函数式选项 (Functional Options) 模式。

### 📦 Python 生态
- **`python-best-practices`** ([ludo-technologies/python-best-practices](https://github.com/ludo-technologies/python-best-practices))
    - **介绍**：Python 现代工程化标准 (Python 3.12+)。涵盖 PEP 8 命名、现代类型提示 (Type Hinting) 及异步处理 (`asyncio`)。
    - **行为**：强制配置并使用现代工具链 (如 `uv`, `ruff`, `mypy`, `pytest`) 替代老旧工具。

### 📦 Java / Spring Boot 生态
- **`java-best-practices`** ([jabrena/cursor-rules-java](https://github.com/jabrena/cursor-rules-java))
    - **介绍**：现代 Java (17/21) 核心开发规范。抛弃老旧模式，拥抱新特性。
    - **行为**：强制要求使用 `Records` 处理不可变数据，使用 `Sealed Classes` 限制继承，利用 `Optional` 避免空指针，以及在 I/O 密集场景默认使用 Virtual Threads (虚拟线程)。
- **`spring-boot-best-practices`** ([jabrena/cursor-rules-java](https://github.com/jabrena/cursor-rules-java))
    - **介绍**：Java 企业级及 Spring Boot 3 现代开发指南。涉及六边形架构 (Hexagonal Architecture)、数据防腐层设计。
    - **行为**：强制使用 Java `Records` 作为 DTO，要求使用 `JOIN FETCH` 等手段避免 JPA 的 N+1 查询问题。优先使用 Testcontainers 进行集成测试。

---

## 8. 数据库与基础设施 (Databases & DevOps)

涵盖关系型数据库的查询调优、架构规范，以及基于 Linux/Docker 的自动化部署。

### 📦 数据库与存储 (Databases & Storage)
- **`sql-best-practices`** ([sanjeed5/awesome-cursor-rules-mdc](https://github.com/sanjeed5/awesome-cursor-rules-mdc))
    - **介绍**：通用 SQL 安全与规范指南。
    - **行为**：强制标识符使用 `snake_case`，使用复数表名与单数列名。严禁拼接 SQL，必须使用预编译语句 (Prepared Statements) 防止注入。
- **`postgres-best-practices`** ([neondatabase/postgres-skills](https://github.com/neondatabase/postgres-skills))
    - **介绍**：PostgreSQL 架构与查询优化指南。
    - **行为**：要求外键必须建立索引，优先使用 CTE (公用表表达式) 而非复杂子查询，并在优化时使用 `EXPLAIN ANALYZE`。
- **`mysql-best-practices`** ([planetscale/database-skills](https://github.com/planetscale/database-skills))
    - **介绍**：面向大规模 MySQL 的性能架构指南。
    - **行为**：要求主键使用 `BIGINT UNSIGNED`，优化分页（避免深分页 `OFFSET`），保证事务内的查询顺序一致以防止死锁。
- **`sqlite-best-practices`** ([tursodatabase/agent-skills](https://github.com/tursodatabase/agent-skills))
    - **介绍**：SQLite 嵌入式/边缘数据库性能指南。
    - **行为**：默认在建连时开启 `WAL` (Write-Ahead Logging) 模式提升并发，并强制开启外键约束 (`PRAGMA foreign_keys = ON`)。
- **`supabase-postgres-best-practices`** ([supabase/agent-skills](https://github.com/supabase/agent-skills))
    - **介绍**：专为 Supabase 环境优化的 Postgres 性能指南。
    - **场景**：处理 RLS (Row Level Security) 性能瓶颈、连接池配置及实时订阅优化。

### 📦 基础设施与运维 (Infrastructure & DevOps)
- **`linux-shell-scripting`** ([claudiodearaujo/linux-shell-scripting](https://github.com/claudiodearaujo/linux-shell-scripting))
    - **介绍**：提供面向生产环境的自动化 Bash 脚本模板与系统监控思路。
- **`docker-deployment`** ([openclaw/agentic-devops](https://github.com/openclaw/agentic-devops) & [akin-ozer/cc-devops-skills](https://github.com/akin-ozer/cc-devops-skills))
    - **介绍**：Docker 容器化与 CI/CD 自动化部署规范。
    - **行为**：强制使用多阶段构建 (Multi-stage builds) 减小镜像体积，严格配置 `.dockerignore`，并在 `Dockerfile` 中设置非 Root 用户运行以保证安全。

---

## 9. 特定领域生态与独立工具 (Domain-Specific & Standalone Tools)

为特定垂直领域或独立工具链提供的专项技能包。

### 📦 Three.js 3D 生态 ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))

这是一个涵盖 WebGL 场景构建、渲染管线和交互处理的全栈 3D 技能包。为了便于配套使用，按 3D 开发流水分组如下：

#### 场景构建与资源 (Core Setup & Assets)
- **`threejs-fundamentals`**
    - **介绍**：处理 Scene, Camera, Renderer, Object3D 树形层级等底座架构。
    - **场景**：项目初始化，或解决坐标系、对象组装和基础渲染循环问题。
- **`threejs-loaders`**
    - **介绍**：处理 GLTF/GLB 模型、HDR 环境、图片等异步资源的加载。
    - **场景**：建立资源加载管线，处理加载进度条 (LoadingManager) 或模型解析。

#### 视觉表现 (Visuals & Shading)
- **`threejs-geometry`** & **`threejs-materials`**
    - **介绍**：处理顶点数据 (BufferGeometry)、实例化渲染 (Instancing) 以及从基础到 PBR 的物理材质系统。
    - **场景**：程序化生成 3D 形状、优化大量重复物体、或调整模型的物理质感 (金属度/粗糙度)。
- **`threejs-lighting`** & **`threejs-textures`**
    - **介绍**：搭建真实的光影环境。包括不同光源、阴影映射投射，以及 UV 贴图、环境纹理映射。
    - **场景**：优化场景立体感，配置复杂的烘焙阴影或 IBL (基于图像的照明)。
- **`threejs-shaders`**
    - **介绍**：编写原生 GLSL 着色器，使用 ShaderMaterial 定制渲染管线。
    - **场景**：实现内置材质无法完成的特殊视觉效果（如顶点变形、扭曲、流光等）。

#### 动画与交互 (Motion & Interactivity)
- **`threejs-animation`**
    - **介绍**：处理关键帧动画、骨骼动画 (Skeletal Animation) 和形变目标 (Morph Targets)。
    - **场景**：播放 3D 模型的内置动作，或利用 GSAP 等实现程序化运镜。
- **`threejs-interaction`**
    - **介绍**：处理 Raycaster 射线检测、控制器 (OrbitControls) 以及鼠标/触摸的屏幕空间转换。
    - **场景**：实现 3D 场景中的物体点击、悬停高亮、拖拽或自定义运镜控制。

#### 后期处理 (Post-processing)
- **`threejs-postprocessing`**
    - **介绍**：基于 EffectComposer 的屏幕空间特效管线。
    - **场景**：添加 Bloom (泛光)、景深 (DOF)、色彩分级或自定义滤镜，大幅提升画面电影感。

### 📦 演示与文档工具
- **`slidev`** ([slidevjs/slidev](https://github.com/slidevjs/slidev))
    - **介绍**：基于 Web 技术的开发者幻灯片构建工具。支持 Markdown 语法、代码高亮、Vue 组件交互和动画。
    - **场景**：需要制作技术分享、培训课件 or 产品演示的幻灯片时。

---

## 10. 元技能与辅助

### 📦 [vercel-labs/skills](https://github.com/vercel-labs/skills)
- **`find-skills`**
    - **介绍**：在技能生态中搜索并评估新技能。

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)
- **`write-a-skill`**
    - **介绍**：辅助设计并编写符合标准的自定义技能（包括 SKILL.md 和目录结构）。
- **`caveman`**
    - **介绍**：切换至极致压缩的低 Token 沟通模式。

---

## 💡 使用小贴士
1. **相似技能如何选？**
   - 想理清产品逻辑？用 `requirements-analysis` 或 `jobs-to-be-done`。
   - 寻找切入点或破除思维盲区？用 `first-principles-thinking` 或 `mckinsey-framework`。
   - 选数据库/技术栈？用 `architecture-decision`。
   - 画图/出方案文档？用 `senior-architect`。
2. **组合拳推荐**：
   - `uxui-evaluator` + `frontend-skill`：做出既美观又符合体验科学的界面。
   - `direct-response-copy` + `marketing-ideas`：全方位提升产品的市场转化率。
   - `diagnose` + `tdd`：解决最难的 `Bug`。
   - `grill-me` + `six-thinking-hats`：挑战并打磨最稳的方案，消除盲区。
