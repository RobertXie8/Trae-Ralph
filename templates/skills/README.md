# Ralph Skills Ecosystem

这里存放了 Ralph 智能体 (AI Agent) 的所有核心技能定义。每个 Skill 都是一个独立的模块，赋予 Ralph 在软件开发生命周期 (SDLC) 特定阶段的专业能力。

## 🌟 技能概览 (Skill Index)


| Skill Name                  | 核心职责 (Core Responsibilities)                                                 | 触发条件 (Trigger)                     |
| --------------------------- | ---------------------------------------------------------------------------- | ---------------------------------- |
| **ralph-planner**           | **项目指挥官**。负责整体迭代规划、里程碑管理、任务分发。                                               | 用户发起新需求、新迭代或需要全局规划时。               |
| **ralph-round-initializer** | **环境初始化**。负责创建项目结构、初始化文档、准备开发环境。                                             | 项目启动 (Round 1) 或新迭代开始 (Round X) 时。 |
| **ralph-func-analyst**      | **需求预分析**。通过人机交互探索功能广度，产出需求参考文档。                                             | 项目早期、需求模糊或需要头脑风暴时。                 |
| **ralph-web-routine**       | **Web 规划主流程**。编排 `Draft -> Critique -> Research -> Simulation -> Lock` 标准循环。 | 进入 Web 项目的规划与分析阶段。                 |
| **ralph-web-requirement**   | **需求细化**。编写 PRD，进行逻辑自查 (Critique) 和运营推演 (Simulation)。                        | 需要编写/更新 PRD，或进行需求评审时。              |
| **ralph-web-architecture**  | **架构设计**。设计技术方案、API 定义、数据库模型。                                                | 需求明确后，进入技术设计阶段。                    |
| **ralph-web-task-planner**  | **任务拆解**。将需求/架构转化为原子化的开发任务 (Task)。                                           | 架构设计完成后，或需求变更触发 Ripple Sync 时。     |
| **ralph-web-test-planner**  | **测试计划**。制定 DevTools 标准的测试策略和验收标准。                                           | 任务拆解后，进入开发前的最后准备。                  |
| **ralph-task-executor**     | **任务执行**。执行具体的编码任务，遵循 R-Loop (TDD) 流程。                                       | 用户明确指令 "开始开发" 或指定某个 Task ID 时。     |
| **ralph-test-executor**     | **测试执行**。运行测试用例，验证功能正确性。                                                     | 任务完成后，或需要回归测试时。                    |
| **ralph-state-manager**     | **状态管理**。维护项目全局状态 (Tasks/Tests 计数)，确保文档一致性。                                  | 每次任务/测试变更后，或 Milestone 结束时。        |


## 📐 标准技能结构 (Standard Structure)

为确保 AI 的理解一致性和可维护性，所有 `SKILL.md` 遵循以下统一结构：

1. **📋 技能描述 (Description)**: 定义“我是谁”，设定角色设定 (Persona) 和核心目标。
2. **🎯 触发条件 (Trigger)**: 定义“何时被调用”，明确上下文和前置条件。
3. **🛠️ 核心职责 (Core Responsibilities)**: 定义“我要做什么”，列出关键产出和能力边界。
4. **⚙️ 执行协议 (Execution Protocol)**: 定义“怎么做”，包含详细的步骤、算法、SOP 或思维链 (CoT)。
5. **🛡️ 铁律与约束 (Iron Rules & Constraints)**: 定义“绝对不能做的事”，包含安全红线、质量标准和禁止行为。

30| 6.  **📂 关联资产 (Related Assets)**: 列出依赖的模板、文档或工具 (e.g., `./assets/template.md`)。

## 🚀 如何使用 (Usage)

### 自动调用

在 `ralph-planner` 或 `ralph-web-routine` 的编排下，Ralph 会根据当前阶段自动加载并执行相应的 Skill。

### 手动调用

用户可以通过对话直接激活特定 Skill：

> "调用 `ralph-func-analyst` 帮我分析一下这个点子。"
> "使用 `ralph-web-task-planner` 重新拆解一下任务。"

## ➕ 如何贡献 (Contribution)

新增 Skill 时，请务必：

1. 在 `templates/skills/` 下新建目录。
2. 创建 `SKILL.md` 文件。
3. **严格复制**并填充上述 6 大标准板块。
4. 在 `SKILL.md` 头部添加 YAML Frontmatter (name, description)。

