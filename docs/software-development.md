# 软件开发主流程

这一页集中放高频查阅的软件工程主链路，尽量覆盖从“想清楚做什么”到“把代码安全交付出去”的全过程。

---

## 需求、方案与架构

### 📦 [jwynia/agent-skills](https://github.com/jwynia/agent-skills)

- **`requirements-analysis` (需求诊断)** ([jwynia/agent-skills](https://github.com/jwynia/agent-skills))
    - **介绍**：它不是简单的文档生成器，而是一个**诊断工具**。它假设所有初始需求都是“假设”，核心目标是区分“用户想要的”和“用户底层的痛苦”。
    - **场景**：当你只有一个模糊想法时，它会追问：谁在受苦？如果不做会怎样？
    - **补充**：会强制产出 `Problem Statement Brief` 和 `Constraint Inventory`，在 `RA5` 之前拒绝进入设计。

- **`system-design` (架构导航)** ([jwynia/agent-skills](https://github.com/jwynia/agent-skills))
    - **介绍**：专注于从需求到 `Walking Skeleton` 的转化。
    - **场景**：需求已经比较清楚，需要明确模块职责、边界、数据流和最小可运行链路时。
    - **补充**：会识别 under-engineering 和 over-engineering 风险，常见产物包括 `Component Map`、数据流向图和 `Walking Skeleton`。

- **`architecture-decision` (关键决策)** ([jwynia/agent-skills](https://github.com/jwynia/agent-skills))
    - **介绍**：当面临数据库选型、服务拆分、接口风格等关键取舍时使用。
    - **场景**：方案里出现昂贵、关键、难回滚的技术决策，需要显式比较 trade-off 时。
    - **逻辑**：基于权衡而不是“完美架构”。
    - **补充**：通常会沉淀为标准 `ADR`。

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)

- **`grill-me` (冷酷追问)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：沿着决策树持续追问，把计划或设计里没想透的分支逐个逼出来。
    - **场景**：想压测方案、找漏洞、确认假设是否站得住时。

- **`grill-with-docs` (约束压测)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：带文档约束的 `grill-me`。
    - **场景**：已有 `CONTEXT.md`、ADR 或重领域术语约束，需要确保新方案不跑偏时。

### 架构与建模补充

- **`domain-driven-design`** ([wondelai/skills](https://github.com/wondelai/skills))
    - **介绍**：基于 DDD 的战术与战略模式，强调通用语言、有界上下文和聚合边界。
    - **场景**：复杂度已经上升到“术语混乱、边界不清、领域概念散落各处”时。

- **`clean-architecture`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：用分层和依赖反转整理服务端项目，把业务规则和框架、存储、交付层解耦。
    - **场景**：handler、service、repository 等职责开始缠在一起，改一层总要连带改很多地方时。

- **`architecture-patterns`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：系统化使用 Clean Architecture、Hexagonal 和 DDD 模式来梳理后端边界与上下文。
    - **场景**：你已经意识到问题不只是代码乱，而是边界模型和依赖方向本身不清晰时。

- **`senior-architect`** ([alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills))
    - **介绍**：偏社区工具箱式的架构辅助 skill，适合补架构图、依赖视图和系统级梳理。
    - **场景**：需要快速产出结构视图、依赖关系草图，或者给较大的代码库补一个高层架构切面时。

### 文档结构、治理与上下文治理

- **`crafting-effective-readmes`** ([softaworks/agent-toolkit](https://github.com/softaworks/agent-toolkit))
    - **介绍**：专注于把 README、总览页和导览页写成符合目标读者预期的入口文档，而不是信息堆砌。
    - **场景**：项目已经有不少内容，但首页仍然像维护者笔记，缺少明确定位、阅读顺序和基本结构时。
    - **补充**：更偏“文档应该长成什么样”，不是单纯润色句子。

- **`readme-blueprint-generator`** ([github/awesome-copilot](https://github.com/github/awesome-copilot))
    - **介绍**：为 README 或概览页提供结构蓝图，帮助先定信息层级，再补具体内容。
    - **场景**：你知道当前入口页不顺，但还说不清到底该先讲定位、目录、使用方式还是维护规则时。
    - **补充**：更适合拿来整理骨架，不必按默认模板原样照搬。

- **`information-architecture`** ([julianoczkowski/designer-skills](https://github.com/julianoczkowski/designer-skills))
    - **介绍**：从信息架构角度梳理文档导航、分类方式和查阅路径，减少读者跳转和迷路成本。
    - **场景**：目录已经变多，或者你开始怀疑“内容本身没问题，问题出在信息放置方式”时。

- **`documentation-and-adrs` (决策留痕)** ([addyosmani/agent-skills](https://github.com/addyosmani/agent-skills))
    - **介绍**：把设计与实现背后的“为什么”沉淀为 `ADR`、技术方案文档、README 结构和关键注释。
    - **场景**：方案已定、公共行为要变化、后续会被反复追问“为什么这么做”时。

- **`project-docs-rules` (文档收口)**（本地技能）
    - **介绍**：给常规软件项目建立一套轻量但稳定的文档治理工作流，把“当前真实架构”“关键决策”“过程 notes”“历史归档”和“AI 首屏入口”分开管理。
    - **场景**：文档开始逐渐变多、变散、重复，或者 AI 总是缺一个稳定入口时。

- **`context-engineering` (上下文工程)** ([addyosmani/agent-skills](https://github.com/addyosmani/agent-skills))
    - **介绍**：把 AI 协作所需的背景、约束、示例和记忆组织成可维护的上下文体系，减少会话漂移和重复解释。
    - **场景**：项目规则、设计文档、历史决策和代码约束已经很多，需要明确“AI 每次应该先读什么、按什么顺序读、哪些内容不该塞进默认上下文”时。

---

## 任务、Issue 与协作

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)

- **`setup-matt-pocock-skills`** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：把 `Issue Tracker`、标签体系和领域文档位置注入给相关工作流技能。
    - **场景**：第一次在一个项目里使用 `to-prd`、`to-issues`、`triage` 这类工作流技能时。

- **`to-prd` (PRD 合成)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：基于当前上下文和代码库理解，自动生成结构完整的 PRD。
    - **场景**：需求和方案已经有一定上下文，需要整理成正式 PRD，而不是继续前期探索时。

- **`to-issues` (垂直切片拆解)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：把大任务拆成可执行 issue，强调垂直切片，而不是按层横向拆。
    - **场景**：要从计划推进到实施，需要把工作拆成可独立验证、可直接领取的切片时。

- **`triage` (状态机管理)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：管理 issue 生命周期，判断是否信息充分、是否适合交给 agent 或人继续推进。
    - **场景**：issue 是否该继续、该补信息、该交给 agent，或者该回到人工处理，需要明确状态判断时。

- **`planning-with-files`** ([OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files))
    - **介绍**：把任务计划和过程记录持久化到文件中，减少长任务上下文丢失。
    - **场景**：任务很长、步骤很多，担心多轮对话后上下文断裂时。

- **`user-stories`** ([product-on-purpose/pm-skills](https://github.com/product-on-purpose/pm-skills))
    - **介绍**：把需求写成面向用户价值的可执行故事单元，帮助需求表达从“想法”过渡到“可实现条目”。
    - **场景**：需求方向已经比较清楚，但还缺一个更贴近实现和协作的表达层时。

- **`acceptance-criteria`** ([product-on-purpose/pm-skills](https://github.com/product-on-purpose/pm-skills))
    - **介绍**：把需求收束成可验证的验收条件，减少“做完了但标准不一致”的情况。
    - **场景**：需求已经写出来，但交付标准仍然模糊，或者开发、测试、产品对完成定义不一致时。

---

## Git / 分支与交付流程

### 📦 [obra/superpowers](https://github.com/obra/superpowers)

- **`using-git-worktrees` (任务隔离)** ([obra/superpowers](https://github.com/obra/superpowers))
    - **介绍**：在开始实现前创建独立 worktree 和分支，避免多个任务混进同一工作区。
    - **场景**：你已经在做一件事，又想并行开另一个需求，或者想从源头控制提交边界时。

- **`finishing-a-development-branch` (分支收口)** ([obra/superpowers](https://github.com/obra/superpowers))
    - **介绍**：在实现完成后明确选择本地合并、推 PR、保留分支或丢弃工作。
    - **场景**：代码已经改完，但你不希望默认“一做完就全推”，而是想把收尾方式显式做成决策时。

- **`commit-work` (原子提交)** ([softaworks/agent-toolkit](https://github.com/softaworks/agent-toolkit))
    - **介绍**：把提交代码从一句 `git add -A && git commit` 变成一套可审查的原子提交流程。
    - **场景**：AI 一次做了多件事、同一文件里混了多种改动，或者你怀疑有些改动不该进这次提交时。

---

## 调试、测试与代码质量

### 📦 [mattpocock/skills](https://github.com/mattpocock/skills)

- **`diagnose` (硬核 Bug 诊断)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：用“反馈回路 -> 复现 -> 假设 -> 探针 -> 修复 -> 回归”的纪律化闭环排查 bug。
    - **场景**：难复现 bug、复杂错误链路、性能回退，或者你还没有稳定复现手段时。
    - **补充**：没有稳定反馈回路之前，不轻易猜原因。

- **`zoom-out` (高层建模)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：先给出高层模块地图和调用关系，再进入局部实现。
    - **场景**：面对不熟悉代码库时，先看地图比先看细节更重要的阶段。

- **`tdd` (测试驱动开发)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：按 red-green-refactor 循环推进，强调先红后绿。
    - **场景**：你希望先锁定行为，再写实现，或者要减少回归风险时。

- **`tech-debt`** ([anthropics/knowledge-work-plugins](https://github.com/anthropics/knowledge-work-plugins))
    - **介绍**：识别并梳理代码库中的技术债，帮助把“哪里越来越乱”从模糊感觉变成可讨论的问题清单。
    - **场景**：逻辑反复打补丁、兜底分支越来越多、层次开始互相污染，但你还没决定先从哪一块下手时。

- **`improve-codebase-architecture` (代码深化)** ([mattpocock/skills](https://github.com/mattpocock/skills))
    - **介绍**：在已有代码库中寻找 deepening opportunities，提升 locality、leverage 和可测试性。
    - **场景**：系统还能跑，但你已经感到模块浅、边界弱、局部改动牵连范围过大时。

- **`code-simplification` (复杂度收敛)** ([addyosmani/agent-skills](https://github.com/addyosmani/agent-skills))
    - **介绍**：在不改行为的前提下收敛复杂度，适合处理中途越写越绕的局部代码。
    - **场景**：代码不是“错了”，而是局部复杂度已经明显高于它应该承载的行为复杂度时。

### 质量收束

- **`code-review`** ([google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli))
    - **介绍**：聚焦真实 bug、规则违反和可验证问题，而不是泛泛风格意见。
    - **场景**：你希望 review 重点落在行为风险、回归点和规则违反，而不是表层格式时。

- **`clean-code`** ([AbsolutelySkilled/AbsolutelySkilled](https://github.com/AbsolutelySkilled/AbsolutelySkilled))
    - **介绍**：围绕命名、函数边界、错误处理、测试和 code smells 建立日常整洁治理基线。
    - **场景**：代码开始变得难读，但问题还没严重到要做大重构时。

---

## 代码理解、复杂度与迁移

- **`understand`** ([Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything))
    - **介绍**：为大型仓库生成可探索的知识图谱，帮助先摸清模块、依赖、入口和跨文件关系。
    - **场景**：第一次接手大仓库，不知道复杂度热点在哪，或者怀疑真实结构和目录结构不一致时。

- **`understand-domain`** ([Lum1104/Understand-Anything](https://github.com/Lum1104/Understand-Anything))
    - **介绍**：从代码理解继续往上抽到业务域、核心流程和 domain flow。
    - **场景**：你真正想弄清的是“系统在做什么”，而不是只看实现细节时。

- **`legacy-modernizer`** ([jeffallan/claude-skills](https://github.com/jeffallan/claude-skills))
    - **介绍**：围绕依赖图、风险登记、characterization tests、回滚策略和 strangler fig 设计旧系统的渐进式迁移路线。
    - **场景**：旧系统体量大、不能大爆炸重写，需要边迁移边保业务和回滚能力时。
