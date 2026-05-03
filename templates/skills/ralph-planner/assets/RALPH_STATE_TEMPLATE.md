# Ralph 项目状态 (Project State)

> **当前上下文 (Current Context)**: 规划阶段 (Planning)
> **迭代名称 (Iteration)**: [此处填写实际迭代名称] (例如: v0.1-alpha, feature-login)

## 1. 规划阶段 (Planning Phase)

> **目标**: 在编码前通过 3 轮迭代完善需求与架构。


| 轮次 (Round)       | 步骤 1: 草稿 (Draft) | 步骤 2: 自查 (Critique) | 步骤 3: 调研 (Research) | 步骤 4: 推演 (Simulation) | 步骤 5: 锁定 (Lock) |
| ---------------- | ---------------- | ------------------- | ------------------- | --------------------- | --------------- |
| **Round 1** (基线) | 🔄 进行中           | ⏳ 待定                | ⏳ 待定                | ⏳ 待定                  | ⏳ 待定            |
| **Round 2** (修订) | ⏳ 待定             | ⏳ 待定                | ⏳ 待定                | ⏳ 待定                  | ⏳ 待定            |
| **Round 3** (终定) | ⏳ 待定             | ⏳ 待定                | ⏳ 待定                | ⏳ 待定                  | ⏳ 待定            |


## 2. 开发阶段 (Implementation Phase)

> **目标**: 严格按顺序执行开发任务。
> **⚠️ 执行铁律**: 必须严格按照 `04-ralph-tasks.md` 中的列表顺序执行任务。**严禁跳跃**或乱序执行。

- **状态**: ⏳ 待定 (Pending)
- **进度**: 0 / 0 任务完成
- **引用**: `docs/planning/[Iteration]/04-ralph-tasks.md`

## 3. 测试阶段 (Testing Phase)

> **目标**: 使用测试计划验证功能。
> **⚠️ 执行铁律**: 必须严格按照 `05-test-plan.md` 中的列表顺序执行测试。**严禁跳跃**或乱序执行。

- **状态**: ⏳ 待定 (Pending)
- **进度**: 0 / 0 测试通过（严禁没有修改 05-test-plan.md 测试状态就修改这里）
- **引用**: `docs/planning/[Iteration]/05-test-plan.md`

## 4. Git 同步 (Version Control)

> **目标**: 在 `05-test-plan.md` 全部通过后再入库与推送，避免未验证代码进入远程。
> **顺序**: 先 `git commit`，再 `git push`；若项目无远程或未配置，须在对应项备注原因。

- **本地提交 (`git commit`)**: [ ] （提交信息说明本次迭代/范围；`git status` 中应无遗漏的已修改源文件）
- **远程推送 (`git push`)**: [ ] （推送到约定远程与分支；不适用则写「N/A」及原因）

## 5. 项目交付 (Project Delivery)

- **最终审查**: [ ]
- **用户验收**: [ ]

