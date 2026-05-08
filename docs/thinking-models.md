# 思维模型与通用分析

这一页集中放“帮助你想清楚问题”的技能。它们通常不直接替你写业务代码，而是帮助你拆问题、找盲区、校准上下文和压测方案。

---

## 通用分析与哲学框架

### 商业逻辑与防盲从分析

- **`mckinsey-framework`** ([nicepkg/ai-workflow](https://github.com/nicepkg/ai-workflow))
    - **介绍**：将金字塔原理、问题树、SCQA 等结构化分析方法引入推演过程。
    - **场景**：问题规模较大、信息很多、容易出现重叠或遗漏，需要先做结构化拆解时。
    - **补充**：强调 MECE，减少重叠和遗漏。

- **`six-thinking-hats`** ([neurofoo/agent-skills](https://github.com/neurofoo/agent-skills))
    - **介绍**：用不同思维角色顺序推演，克服单一路径思考。
    - **场景**：讨论已经陷入单一路径，或者你怀疑团队在某一种视角上用力过猛时。

- **`brainstorming`** ([obra/superpowers](https://github.com/obra/superpowers))
    - **介绍**：通过一轮轮提问和候选方案比较，把模糊想法打磨成可进入需求分析或设计阶段的方案草稿。
    - **场景**：只有一个方向、还没形成清晰方案，想先比较 2-3 条路线时。

- **`mom-test`** ([wondelai/skills](https://github.com/wondelai/skills))
    - **介绍**：围绕《The Mom Test》的思路改写用户访谈提问方式，避免把访谈做成“收集礼貌性认同”。
    - **场景**：产品还在早期，准备做用户访谈，但你担心问法会把结果带偏时。
    - **组合**：适合作为 `requirements-analysis`、`jobs-to-be-done` 或用户研究前的提问校准器。

### 哲学与第一性原理

- **`socratic-questioning`** ([neurofoo/agent-skills](https://github.com/neurofoo/agent-skills))
    - **介绍**：通过连续追问识别隐藏假设，推动澄清主张、证据和推论。
    - **场景**：一个观点听起来很顺，但你怀疑背后有未经检查的前提时。

- **`first-principles-thinking`** ([akshat10/skills](https://github.com/akshat10/skills))
    - **介绍**：拒绝直接类比，从最基础、最不可辩驳的前提重新推导方案。
    - **场景**：你已经发现“行业惯例”可能不适用，或者要重新审视一个默认被接受的方案时。

- **`thinking-partner`** ([mattnowdev/thinking-partner](https://github.com/mattnowdev/thinking-partner))
    - **介绍**：把 Agent 变成“智力陪练”，帮助挑战潜意识假设并暴露思维盲区。
    - **场景**：你不一定缺答案，但缺一个能持续追问、反驳和拉开视角的对话对象时。

---

## 产品与策略方法

- **`jobs-to-be-done`** ([wondelai/skills](https://github.com/wondelai/skills))
    - **介绍**：基于 JTBD 理论，把讨论重点从“功能堆砌”转到“目标结果”。
    - **场景**：团队一直在堆功能，但你更想先搞清楚用户到底在“雇佣”产品做什么时。

- **`design-thinking`** ([melodic-software/design-thinking](https://github.com/melodic-software/design-thinking))
    - **介绍**：沿着 Empathize、Define、Ideate、Prototype、Test 这条路径推进问题探索。
    - **场景**：产品极早期、方向不稳，或者你需要从需求理解一路推进到原型验证时。

- **`design-sprint`** ([wondelai/skills](https://github.com/wondelai/skills))
    - **介绍**：用短周期冲刺的方式快速验证想法，把讨论尽快推进到原型和反馈，而不是长时间停留在抽象规划里。
    - **场景**：方向还没完全确定，但已经需要快速验证方案、交互或价值假设时。
    - **组合**：比 `brainstorming` 更偏收敛和验证；在进入完整 PRD 或系统设计之前很适合用来做中间验证。
