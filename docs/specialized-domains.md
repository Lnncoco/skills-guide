# 专项领域与独立能力

这一页集中放那些明显带有领域边界的技能。它们很有用，但不应该和通用软件开发主流程或语言生态混在一起。

---

## Web3 与区块链

- **`solidity`** ([mindrally/skills](https://github.com/mindrally/skills))
    - **介绍**：聚焦 Solidity 合约开发本身，覆盖语言习惯、合约组织和常见工程约束。
    - **场景**：项目明确进入智能合约实现、合约阅读或合约重构阶段时。

- **`solidity-security`** ([wshobson/agents](https://github.com/wshobson/agents))
    - **介绍**：聚焦 Solidity 合约安全、常见攻击面和审查要点，适合把安全约束前置到实现和 review 过程。
    - **场景**：你在写或审查 Solidity 合约，需要把重入、权限控制、外部调用和升级风险放到最高优先级时。

---

## Three.js 3D 生态

### 📦 [cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills)

#### 场景构建与资源

- **`threejs-fundamentals`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：处理 Scene、Camera、Renderer、Object3D 层级等底座架构。
    - **场景**：项目初始化，或者你还在处理坐标系、渲染循环和对象层级这些底座问题时。

- **`threejs-loaders`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：处理 GLTF / GLB、HDR、图片等异步资源加载。
    - **场景**：需要建立资源加载管线、处理模型解析或加载进度时。

#### 视觉表现

- **`threejs-geometry`** & **`threejs-materials`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：处理几何体、实例化渲染以及从基础到 PBR 的材质系统。
    - **场景**：要程序化生成形状、优化大量重复物体，或者调整材质表现时。

- **`threejs-lighting`** & **`threejs-textures`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：搭建光影环境、阴影映射、UV 贴图和环境纹理。
    - **场景**：需要提升立体感、配置阴影、环境贴图或整体光照氛围时。

- **`threejs-shaders`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：编写 GLSL 着色器，定制渲染管线。
    - **场景**：内置材质不够用，需要做顶点变形、扭曲、流光等特殊视觉效果时。

#### 动画与交互

- **`threejs-animation`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：处理关键帧动画、骨骼动画和 Morph Targets。
    - **场景**：要播放模型内置动作，或者做程序化运镜和状态过渡时。

- **`threejs-interaction`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：处理 Raycaster、控制器和鼠标 / 触摸交互。
    - **场景**：需要做点击、悬停、拖拽、选中或用户控制视角时。

#### 后期处理

- **`threejs-postprocessing`** ([cloudai-x/threejs-skills](https://github.com/cloudai-x/threejs-skills))
    - **介绍**：基于 EffectComposer 的屏幕空间特效管线。
    - **场景**：要加 Bloom、景深、色彩分级或其他屏幕空间特效时。

---

## 演示与独立工具

- **`slidev`** ([slidevjs/slidev](https://github.com/slidevjs/slidev))
    - **介绍**：基于 Web 技术的开发者幻灯片构建工具，支持 Markdown、代码高亮、Vue 组件交互和动画。
    - **场景**：需要制作技术分享、培训课件或产品演示型幻灯片时。
