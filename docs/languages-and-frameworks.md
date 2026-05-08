# 语言与框架生态

这一页集中放语言、框架和工程生态本身的技能，便于按技术栈查阅。

---

## JavaScript / TypeScript 与工程规范

- **`javascript-mastery`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：深度讲解 33+ 个 JS 核心概念，提升底层理解。
    - **场景**：你不是缺 API，而是缺对闭包、原型链、事件循环、this、异步模型这些基础机制的稳定理解时。

- **`typescript-advanced-types`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：设计复杂泛型、条件类型及类型推导逻辑，适合高阶类型编程。
    - **场景**：需要构建类型安全库、复杂组件 API，或者要把运行时约束尽量前移到编译期时。

### 📦 [antfu/skills](https://github.com/antfu/skills)

- **`antfu`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：提供 Anthony Fu 风格的项目组织、代码约定、工具选择和 lint / 格式化路线。
    - **场景**：你想给 TS / JS 项目建立一套更完整、更一致的工程风格时。

- **`pnpm`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：聚焦 PNPM 的 workspace、catalog、patch、override、store 和依赖管理方式。
    - **场景**：多包仓库、依赖治理、版本收口或 catalog 管理是当前重点时。

- **`vite`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：处理 Vite 配置、插件、SSR 和构建问题。
    - **场景**：需要调整 Vite 配置、排查构建问题，或者编写插件时。

- **`vitepress`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：处理 VitePress 文档站的配置、主题和内容能力。
    - **场景**：搭文档站、知识库或产品文档官网时。

- **`vitest`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：处理 Vitest 的测试组织、mock、过滤和 coverage。
    - **场景**：项目本身已经使用 Vite 生态，想要更自然地补单测或改测试配置时。

- **`tsdown`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：围绕 tsdown 做库打包、声明生成和多格式输出。
    - **场景**：构建 TypeScript / JavaScript 库，且你关心打包速度、声明输出或格式兼容时。

- **`turborepo`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：围绕 monorepo 的任务图、缓存、边界和 CI 配置工作。
    - **场景**：仓库已经进入多包协作阶段，需要任务编排、缓存和 CI 加速时。

- **`unocss`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：处理 UnoCSS 的 presets、规则、shortcuts 和属性化写法。
    - **场景**：项目使用 UnoCSS，或者你想搭一个更偏原子化、即时生成的样式体系时。

---

## Vue / Nuxt 生态

- **`vue`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：Vue 3 通用能力入口，覆盖 Composition API、SFC、内建组件和基础响应式模型。
    - **场景**：需要查询 Vue 3 的基础能力、SFC 结构或响应式模型时。

- **`nuxt`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：处理 Nuxt 的 SSR、auto-import、文件路由、server routes 和混合渲染能力。
    - **场景**：项目明确使用 Nuxt，需要处理数据获取、路由、服务端逻辑或渲染策略时。

- **`pinia`** ([antfu/skills](https://github.com/antfu/skills))
    - **介绍**：从“工具本身”角度处理 Pinia 的 store、getter、action 和插件能力。
    - **场景**：你需要了解 Pinia 官方能力边界、基础 API 模式或插件机制时。

- **`vueuse-functions`** ([vueuse/skills](https://github.com/vueuse/skills))
    - **介绍**：面向 Vue / Nuxt 的可复用组合式工具集，帮助用现成 composables 更快表达常见响应式需求。
    - **场景**：你发现自己在反复写监听窗口、存储同步、事件订阅、计时器、状态桥接这类常见组合式逻辑时。

- **`vue-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：Vue 项目的默认最佳实践入口，强调 Vue 3、Composition API、`<script setup>` 和 TypeScript。
    - **场景**：一般 Vue 项目开发、组件设计、组合式 API 使用和整体规范制定时。
    - **补充**：默认开启组合式写法，内置组件拆分触发器。

- **`vue-debug-guides`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：集中处理响应式异常、异步失败和 hydration 问题。
    - **场景**：项目出现难解释的运行时异常、响应式丢失或 SSR / hydration 问题时。

- **`vue-pinia-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：从“使用策略”角度处理 Pinia store 设计和响应式边界。
    - **场景**：你已经决定用 Pinia，但重点问题在 store 拆分、状态建模和边界控制时。

- **`vue-router-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：处理导航守卫、路由参数和路由组件生命周期模式。
    - **场景**：当前问题集中在路由结构、导航逻辑、守卫和路由行为时。

- **`vue-testing-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：处理 Vue 测试设计，覆盖 Vitest、Vue Test Utils 和 E2E 场景。
    - **场景**：要为 Vue 组件和页面补测试，或者重构现有测试结构时。

- **`create-adaptable-composable`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：教你编写接受 plain value、ref 或 getter 的库级 composable。
    - **场景**：你在做高级 composable、可复用工具函数，或者希望 API 同时兼容值、ref 和 getter 时。

- **`vue-jsx-best-practices`** & **`vue-options-api-best-practices`** ([vuejs-ai/skills](https://github.com/vuejs-ai/skills))
    - **介绍**：分别处理 Vue JSX / TSX 场景，以及 Vue 3 Options API 风格下的常见约束。
    - **场景**：项目显式使用 JSX / TSX 或历史项目明确要求 Options API 时。

---

## React / Next.js 生态

- **`react-best-practices`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：Vercel 官方发布的 React 性能与架构指南。
    - **场景**：React / Next 项目已经跑起来，但你更关心性能、边界和实现质量时。
    - **补充**：强调并行数据获取、减少异步瀑布流，以及在服务端边界内做正确约束。

- **`vercel-react-best-practices`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：围绕 React / Next.js 的性能与实现质量给出高优先级最佳实践，适合写新代码和做代码审查时直接套用。
    - **场景**：你希望 React / Next 项目的默认实现方式更稳，而不是只在性能出问题时再回头补救。

- **`vercel-react-view-transitions`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：指导如何基于原生 View Transition API 做页面切换、共享元素动画和状态过渡。
    - **场景**：想给 React / Next 页面加 route transitions、共享元素过渡或更接近原生应用的切换体验时。

- **`vercel-composition-patterns`** ([vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills))
    - **介绍**：围绕 compound components、context providers 和可组合 API 设计 React 组件。
    - **场景**：组件已经开始出现 props 蔓延、条件分支过多，或者你想整理更可扩展的组件 API 时。

- **`nextjs-app-router`**（社区最佳实践）
    - **介绍**：针对 Next.js App Router 模式的边界划分。
    - **场景**：项目明确使用 App Router，需要处理 `use client` / `use server` 边界或路由组织方式时。

---

## Node.js 生态

- **`nodejs-development`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：提供 Node.js 开发规范与 TypeScript 实践，适合处理服务端项目结构、通用后端实现和 Node 侧工程约定。
    - **场景**：Node.js 服务端项目需要建立比较稳定的项目结构、实现习惯和 TypeScript 基线时。

- **`fastify-typescript`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：围绕 Fastify + TypeScript 的 API 开发，补齐验证、插件、数据库集成和测试实践。
    - **场景**：项目明确使用 Fastify，重点问题在框架层结构、验证和插件组织时。

- **`backend-dev-guidelines`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：强调 `Routes -> Controllers -> Services -> Repositories` 的分层架构。
    - **场景**：你希望后端代码导航更稳定，或者要把服务端代码从“全堆在一起”拉回分层结构时。

- **`nodejs-best-practices`** ([sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills))
    - **介绍**：关于 Node 框架选型、异步流控、错误处理和生产环境安全的深度指南。
    - **场景**：当前问题不只是写业务接口，而是要判断框架方向、异步模式、错误处理和安全基线时。

---

## Go 生态

- **`golang-pro`** ([jeffallan/claude-skills](https://github.com/jeffallan/claude-skills))
    - **介绍**：更完整地覆盖 Go 的惯用写法、包组织、错误处理、接口边界、并发模型和工程实现习惯。
    - **场景**：你在写 Go，但担心自己在套用别的语言习惯，或者需要一套更完整的 Go 开发基线时。

- **`golang-testing`** ([samber/cc-skills-golang](https://github.com/samber/cc-skills-golang))
    - **介绍**：围绕 table-driven tests、subtests、benchmarks、fuzzing 和覆盖率建立更稳的 Go 测试习惯。
    - **场景**：要给 Go 代码补测试、做回归测试或性能基准时。

- **`go-best-practices`** ([samber/cc-skills-golang](https://github.com/samber/cc-skills-golang))
    - **介绍**：Golang 综合最佳实践，覆盖并发、错误处理、表驱动测试及 `context.Context` 传播。
    - **场景**：需要一套更完整的 Go 开发基线，而不是只解决单点问题时。

- **`bubbletea`** ([GGPrompts/TFE](https://github.com/GGPrompts/TFE))
    - **介绍**：围绕 Bubble Tea 的 `model / update / view` 模式、消息流和常见组件组织方式给出针对性指导。
    - **场景**：你要写 Go 终端界面，或者已经在处理消息流、状态更新和组件拆分这类 Bubble Tea 典型问题时。
    
---

## Java / Spring Boot 生态

- **`java`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：补足 Java / Spring Boot / 企业式分层语境，适合理解旧系统源码和职责链。
    - **场景**：你面对的是 Java / Spring Boot 历史项目，首先需要看懂控制层到服务层的职责关系时。

- **`java-springboot`** ([github/awesome-copilot](https://github.com/github/awesome-copilot))
    - **介绍**：覆盖现代 Java 与 Spring Boot 的常见工程实践，包含项目结构、分层、依赖注入、数据访问和测试组织。
    - **场景**：项目明确基于 Spring Boot，需要继续写业务代码、调整分层结构或补测试基线时。

---

## Python 生态

- **`python-best-practices`** ([0xbigboss/claude-code](https://github.com/0xbigboss/claude-code))
    - **介绍**：围绕 Python 工程实践提供更完整的现代开发基线，覆盖项目结构、类型提示、可维护性和常见代码约束。
    - **场景**：想给 Python 项目补更现代的工程基线，而不是只看某个单点语法时。

- **`fastapi`** ([fastapi/fastapi](https://github.com/fastapi/fastapi))
    - **介绍**：围绕 FastAPI 的路由、依赖注入、请求校验、异步处理和 OpenAPI 集成提供框架级指导。
    - **场景**：项目明确使用 FastAPI，需要处理 API 结构、依赖注入、Pydantic 模型或异步接口时。

- **`python-testing-patterns`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：覆盖 Python 测试组织、pytest 风格、fixture 设计、mock 策略和测试边界划分。
    - **场景**：要给 Python 服务补单测、接口测试或重构现有 pytest 结构时。

- **`django-python`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：聚焦 Django 的项目结构、ORM、视图层和常见服务端开发模式。
    - **场景**：项目明确使用 Django，或者你需要维护历史 Django 服务时。
