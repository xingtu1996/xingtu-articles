---
title: 改 1 个配置，AI 编程账单肉眼可见地瘦了
seo_core: Claude Code 省 token / 配置
seo_long: outputStyle concise、AI 编程降本配置、多模型 token 适配
platform_note: 全平台省钱实操；小红书/掘金高收藏
desensitize: 配置为公开能力，可直接发布；deepseek[1m] 为公开模型特性
diagram: 配置清单表 + Concise 前后对比示意（表格/截图）
---

# 改 1 个配置，AI 编程账单肉眼可见地瘦了

> 核心词：Claude Code 省 token｜长尾词：outputStyle Concise、AI 编程降本配置、多模型 token 适配

用 AI 编程工具久了，账单才是真正的"沉默成本"。我最近把 Claude Code 的回复配置从默认改成 `Concise`，再调了一个压缩阈值，实测下来**输出侧肉眼可见地瘦了**。这些东西全是官方文档里写着的，但很多人不知道——今天一次性讲清楚。

---

## 一、核心发现：`outputStyle: "Concise"`

这是最划算的一行配置。

| 项 | 值 |
|----|-----|
| 配置名 | `outputStyle`（写在 settings.json）|
| 值 | `"Concise"` |
| 引入版本 | v2.1.237，**没有环境变量形式** |
| 机制 | 改系统提示词：先给结果、跳过铺垫/复述、默认简短；报错/安全/破坏性确认**完整保留** |
| 生效 | 会话启动读入 system prompt，改后需 `/clear` 或新会话 |
| 作用域 | **只影响主对话，子 agent（subagent）不受影响** |

关键认知：**Concise 是"系统级默认声音"，和你只是口头说"简短点"不一样**——它是写进 system prompt 的兜底。它和另一个叫 Caveman 的强压缩技能是**互补**关系：Concise 管日常默认简洁，Caveman 管极端场景的 ~65% 压缩。

> 配图建议（Concise 前后对比）：左"默认回复：先复述需求→计划→代码→总结"；右"Concise：直接给代码+1 行说明"。

---

## 二、Token 节省配置清单（逐条可抄）

| 配置 | 位置 | 当前 | 建议 | 作用 |
|------|------|:---:|:---:|------|
| `outputStyle: "Concise"` | settings.json | 未设 | ✅ 加 | 输出 token 系统级减少 |
| `CLAUDE_CODE_AUTO_COMPACT_WINDOW` | env/settings | 1048576（顶到 1M） | **800000** | 压缩阈值留缓冲，对齐 80% 标准 |
| `skillListingMaxDescChars` | settings.json | 1024 ✓ | 保持 | skill 描述截断（输入侧）|
| `skillListingBudgetFraction` | settings.json | 默认 0.01 | 保持 | skill 列表占比上限 |
| `CLAUDE_CODE_EFFORT_LEVEL` | env | 未设 | 可选 | 降 effort 省 token（会降质量，谨慎）|
| `MAX_THINKING_TOKENS` | env | 未设 | 可选 | deepseek 路由关思考省 token |
| `BASH_MAX_OUTPUT_LENGTH` | env | 默认 30000 | 可调 | bash 输出截断（间接省）|

**我的实测决策（2026-08-25）**：
- `outputStyle: Concise` → **加入**（用户级 settings），兜底日常简洁，安全内容保留。
- `AUTO_COMPACT_WINDOW` 1M → **下调到 800k**，避免贴上限触发压缩。
- `EFFORT_LEVEL` / `THINKING` → **暂不**，降 effort 影响质量，先观察。

⚠️ **一个坑**：Concise 下模型不写 plan、不复述。如果你们团队 review 依赖"它复述一遍计划"，体验会变（官方 issue 里有人吐槽）。建议**先在非关键会话试跑**。

---

## 三、多模型适配注意（deepseek[1m] 用户必看）

如果你像我一样用带 `[1m]` 后缀的模型（比如 deepseek[1m]），有两个坑：

- 模型 ID 含 `[1m]` 时，`CLAUDE_CODE_MAX_CONTEXT_TOKENS` **不独立生效**——必须设 `CLAUDE_CODE_DISABLE_1M_CONTEXT=1` 才能覆盖。
- `AUTO_COMPACT_WINDOW` 默认 1M = 压缩点顶到极限，调到 800k 才合理。

---

## 四、一句话抄作业

1. settings.json 加 `"outputStyle": "Concise"`；
2. 环境变量把 `AUTO_COMPACT_WINDOW` 设 `800000`；
3. 用 deepseek[1m] 的，记得 `DISABLE_1M_CONTEXT=1` 才能调上下文上限；
4. 先用非关键会话试跑，确认团队 review 体验不吃亏。

这 4 条，零成本，纯官方能力。AI 编程的成本，很多时候不是"用太多"，是"配置没对"。

> 「金句」：**AI 编程的真实成本，一半藏在你的配置文件里。**

---

### 平台微调（多平台差异化）
- **小红书**：清单体图卡，"抄作业 4 条"直接可做收藏贴。
- **掘金**：保留配置表 + 多模型适配，标题《Claude Code 省 token 配置清单：Concise + 压缩阈值》。
- **公众号**：故事化"我怎么发现账单变瘦的"，深度一点。

> 参考：[Output styles](https://code.claude.com/docs/en/output-styles) / [Settings](https://code.claude.com/docs/en/settings) / [Env vars](https://code.claude.com/docs/en/env-vars)。
