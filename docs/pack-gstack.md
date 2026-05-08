# pack-gstack

### 📦 [garrytan/gstack](https://github.com/garrytan/gstack)

  - **介绍**：一个面向 AI 工程工作的成体系技能集。它不是单个 skill 仓库，而是一整套围绕方案评审、工程评审、设计审查、QA、browser 自动化、安全约束、部署和回顾组织起来的 workflow stack。官方在 `agents/openai.yaml` 中把它描述为 “AI builder framework” 和 “full PM/dev/eng/CEO/QA in a box”。

---

## 规划与评审

- **`office-hours`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：偏产品早期的方向校准工具，内置两种模式：更偏 startup 的 forcing questions，以及更偏 builder 的设计思考式 brainstorming。
    - **场景**：项目还在很早期，你怀疑问题定义、需求强度或切入点本身可能站不住时。

- **`autoplan`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：自动串联 CEO、设计、工程、DevEx 评审 skill，形成一条完整的 plan review pipeline，并替你处理大部分中间决策。
    - **场景**：已经有一版方案或计划，希望快速跑完多视角评审，而不是手动逐个调用 review skill 时。

- **`plan-ceo-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：用 CEO / founder 视角重看问题本身，挑战前提、重新判断范围和 ambition，寻找更高价值的产品方向。
    - **场景**：计划看起来“能做”，但你还不确定它是不是值得做、做大还是做小的时候。

- **`plan-eng-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：从工程经理视角锁定执行计划，重点看架构、数据流、边界、测试和性能。
    - **场景**：需求方向已经比较清楚，现在更关心实现路径是否稳、边界是否清楚、测试是否够时。

- **`plan-design-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：用设计评审方式检查方案的界面与体验质量，找出离“10 分设计”还有多远。
    - **场景**：方案已经涉及用户界面、体验流程或视觉表达，想提前评估体验质量而不是等做完再返工时。

- **`plan-devex-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：从开发者体验角度评审方案，关注上手路径、摩擦点、反馈质量和魔法时刻。
    - **场景**：做的是平台、工具、SDK、文档站或其他面向开发者的产品能力时。

- **`plan-tune`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：调整 gstack 内部提问敏感度和使用偏好，帮助整套评审流程更贴近团队习惯。
    - **场景**：你已经开始频繁使用 gstack，但感觉它的提问方式、默认倾向或评审节奏还需要校准时。

---

## 设计与界面

- **`design-consultation`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：先理解产品和设计环境，再提出完整设计系统，包括审美、排版、颜色、布局、间距和动效方向，并把结果沉淀成 `DESIGN.md`。
    - **场景**：产品还缺一条整体设计方向线，不只是要一个页面，而是要一套视觉和体验语言时。

- **`design-shotgun`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：快速生成多套设计变体，做横向对比，再收敛到更有说服力的方向。
    - **场景**：想先放开探索多个视觉方向，而不是一开始就押注单一方案时。

- **`design-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：偏“设计师之眼”的 QA，专门抓视觉不一致、间距问题、层级失衡、AI slop 痕迹和慢交互。
    - **场景**：界面已经做出来，但你怀疑完成度、细节一致性或交互质感还不够时。

- **`design-html`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：在设计方向明确后，生成更接近生产质量的 HTML / CSS 落地稿，承接前面的设计探索与评审结果。
    - **场景**：设计方向已经定下来，希望快速拿到更接近可交付质量的前端实现时。

---

## QA、Review 与交付

- **`qa`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：系统化测试 Web 应用，发现 bug 后继续回到源码修复，并反复验证；支持 Quick、Standard、Exhaustive 三档测试强度。
    - **场景**：你想让一轮 QA 不只是报问题，而是直接形成“发现问题 -> 修复 -> 回归”的闭环时。

- **`qa-only`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：只做 QA 测试和结构化报告，不进入修复阶段。
    - **场景**：当前只需要测试报告、截图和复现步骤，不希望这个流程自动修改源码时。

- **`review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：在落地前对 PR / diff 做结构性审查，重点抓 SQL 安全、LLM trust boundary 和高风险实现问题。
    - **场景**：代码已经改完，准备合并前需要一轮偏风险和结构问题的审查时。

- **`ship`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：围绕测试、review、版本号、changelog、commit、push、PR 创建组织一条完整的交付路径。
    - **场景**：你不是只想提交代码，而是想把“交付前要做的那一整套事”串成稳定流程时。

- **`land-and-deploy`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：承接 `ship` 之后的合并、等待 CI、等待部署和上线后验证。
    - **场景**：PR 已经准备好，接下来重点是把它安全地合并、部署并验证线上状态时。

- **`document-release`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：发布后回头同步 README、ARCHITECTURE、CONTRIBUTING、CLAUDE 等文档，避免交付和文档脱节。
    - **场景**：一次交付已经改动了用户行为、使用方式或工程约定，需要把文档也同步到最新状态时。

- **`canary`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：上线后的 canary 监控，关注控制台报错、性能退化、页面失败和关键截图变化。
    - **场景**：代码刚上线，最关心的是“有没有明显坏掉”而不是继续做下一轮开发时。

- **`health`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把类型检查、lint、测试、死代码检测等工具结果汇总成一张代码质量健康看板。
    - **场景**：你想知道当前仓库的整体工程健康度，而不是逐个去跑和看零散工具输出时。

- **`landing-report`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：查看与发布相关的队列状态、VERSION 占用和兄弟工作区的潜在冲突。
    - **场景**：多人并行交付、多个工作区同时推进时，需要先看清“谁会撞车”再决定怎么发版时。

- **`retro`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：基于提交历史、工作模式和质量指标做工程 retrospective。
    - **场景**：一轮工作结束后，不想只凭感觉复盘，而是希望从提交和质量数据中抽问题时。

---

## 浏览器与网页自动化

- **`browse`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：gstack 的 headless browser 核心能力，用于打开页面、交互、截图、验证状态、测试表单 / 上传 / dialog，并收集证据。
    - **场景**：任何需要“真的去打开页面看一眼，而不是只读代码猜”的时候，都很适合先想到它。

- **`scrape`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：从网页中提取结构化数据，第一次先原型化抓取流程，后续再路由到更稳定、可复用的 browser skill。
    - **场景**：你要从页面里稳定抽数据，但还不确定最合适的抓取路径时。

- **`skillify`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把最近一次成功的 `/scrape` 流程固化成永久 browser skill，方便后续快速复用。
    - **场景**：某个 scrape 流程已经被证明可行，而且你预计后面会重复执行时。

- **`pair-agent`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：让远端 AI agent 和你的浏览器配对，形成带浏览器能力的协同调试或评审过程。
    - **场景**：你需要另一个 agent 也能共享浏览器上下文，而不是只能靠文字转述页面状态时。

- **`open-gstack-browser`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：启动 gstack 自带的浏览器和侧边栏，用可视方式观看 AI 在浏览器里的动作。
    - **场景**：你希望把浏览器操作显式地看在眼里，或者需要边看边确认自动化行为时。

- **`setup-browser-cookies`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把你真实浏览器里的 cookie 导入到 gstack 的 headless browse 会话中。
    - **场景**：测试流程依赖登录态、真实站点会话或某些你本地已有的身份状态时。

- **`make-pdf`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把 Markdown 文档转成更适合发布或交付的 PDF。
    - **场景**：需要把计划、报告、方案或说明文档整理成更正式、可分发的交付物时。

- **`setup-deploy`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：配置 `land-and-deploy` 所需的部署参数，包括平台识别、生产 URL 和健康检查方式。
    - **场景**：准备把 `ship` / `land-and-deploy` 接到真实部署环境上，但当前还没有明确部署平台或健康检查配置时。

---

## 安全、约束与调查

- **`careful`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：在执行删除、强推、重置、危险数据库操作等高风险动作前给出显式提醒。
    - **场景**：这轮工作可能涉及删除、强制覆盖或不可逆操作，但你仍想继续保留人工确认这一道门槛时。

- **`freeze`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把当前会话的文件改动范围冻结在特定目录里，避免顺手改到别处。
    - **场景**：你只想让这轮修改严格限制在某个目录、某个模块或某个工作区内时。

- **`guard`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把 `careful` 和 `freeze` 组合起来，形成更严格的安全执行模式。
    - **场景**：你既担心改到不该改的文件，也担心误执行危险命令，想同时收紧两层约束时。

- **`unfreeze`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：解除 `freeze` 设定的目录边界。
    - **场景**：之前为了收缩改动范围做了冻结，现在需要重新放开编辑范围时。

- **`cso`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：从安全负责人的角度做基础设施、安全边界、依赖供应链和 CI / CD 审查。
    - **场景**：当前重点不只是功能对不对，而是基础设施、供应链和平台层面有没有明显安全风险时。

- **`investigate`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：偏 root-cause 的系统化排错流程，强调先调查、再分析、再假设、最后实现修复。
    - **场景**：问题复杂、线索分散、你已经发现“直接修”很可能只是碰运气时。

- **`devex-review`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：通过真实浏览器操作去审查开发者体验，测试文档、getting started 流程、错误提示和上手摩擦点。
    - **场景**：你不是想抽象讨论 DevEx，而是想真的跑一遍开发者路径，看看新人会在哪卡住时。

---

## 上下文、记忆与状态

- **`context-save`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：保存当前工作上下文，包括 git 状态、关键决策和未完成事项，方便后续接续。
    - **场景**：你准备暂停、切换上下文、跨设备继续，或者担心这轮推理链会在下一次会话里丢掉时。

- **`context-restore`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：恢复之前保存的上下文，让后续会话更快进入状态。
    - **场景**：你不是从零开始，而是要把之前一轮中断的工作重新接起来时。

- **`learn`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：管理 gstack 在多轮使用中积累的项目 learnings。
    - **场景**：你已经开始积累一些长期有效的经验、约束或习惯，希望把它们系统化保存时。

- **`setup-gbrain`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：给 gstack 安装和初始化持久记忆层 gbrain。
    - **场景**：你希望 gstack 不再只依赖当前会话上下文，而是开始拥有可持续的外部记忆能力时。

- **`sync-gbrain`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：让 gbrain 跟随仓库代码变化持续同步，并刷新相关搜索与上下文提示。
    - **场景**：gbrain 已经在用，但仓库最近变化很多，你担心它的记忆或索引已经过时了时。

---

## Benchmark、模型与宿主桥接

- **`benchmark`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：围绕 browse 能力做性能回归检测，关注页面加载时间、Core Web Vitals 和资源体积。
    - **场景**：你怀疑前后两次改动之间有性能回退，或者需要把性能变化量化成对比结果时。

- **`benchmark-models`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把同一个 skill 或 prompt 放到不同模型上并排比较，衡量延迟、token、成本和效果差异。
    - **场景**：你在评估模型选型，或者想知道同一工作流在 Claude、GPT、Gemini 上的实际差异时。

- **`codex`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：把 OpenAI Codex CLI 包装进 gstack 体系中，支持 review、challenge 和咨询等模式。
    - **场景**：你已经在 gstack 工作流里，但想把 Codex 的能力嵌进这套体系中统一调用时。

- **`gstack-upgrade`** ([garrytan/gstack](https://github.com/garrytan/gstack))
    - **介绍**：升级 gstack 本身并展示版本变化。
    - **场景**：怀疑当前版本落后，或者准备统一升级 gstack 并确认变更内容时。
