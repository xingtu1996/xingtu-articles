# xingtu-articles · 行途文章库

![Articles](https://img.shields.io/badge/articles-38-blue.svg) ![License](https://img.shields.io/badge/license-CC%20BY--SA%204.0-green.svg)

公众号「**行途 XingTu**」已发布文章的公开镜像库：正文 Markdown + 配图素材包，按年月归档。

> 首发均在公众号，本仓为可检索归档。可视化浏览见 👉 [文章星图](https://xingtu1996.github.io/articles.html)

## 📂 目录结构与命名规则

```
articles/YYYY/MM/YYYY-MM-DD-<english-slug>.md   # 正文（frontmatter 含 title/date/slug/summary/category）
assets/YYYY/MM/<同名slug>/                       # 该文的配图素材包（cover.png = 封面）
assets/shared/                                   # 多篇共用图
notes/                                           # 调研笔记（非发布文章）
tuitu/                                           # 贴图卡（社交分发用）
index.json                                       # 机器可读清单（含 prev/next/related_repos）
```

**命名规则**：`YYYY-MM-DD-<英文slug>.md`，素材包目录与文件同名；每篇 frontmatter 必含 `title / date / slug / summary / category`。

## 🆕 最新 10 篇

| 日期 | 标题 | 分类 |
|------|------|------|
| 2026-10-21 | [项目范围越失控，客户越满意？一个 FDE 项目的真相](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-21-project-scope-out-of-control-fde.md) | 📌 FDE实战 |
| 2026-10-20 | [我说了句「改吧」，AI 就不按规矩来了？](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-20-two-words-bypass-process.md) | 📌 AI 工程化实践 |
| 2026-10-19 | [你的 AI 护栏装了等于没装：三种静默失效](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-19-ai-guardrail-three-silent-failures.md) | 📌 AI 工程化实践 |
| 2026-10-17 | [写方案前，先让 10 个 AI 角色互怼](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-17-ai-roles-debate-before-plan.md) | 🔧 FDE · AI 工程化落地 |
| 2026-10-16 | [从 AI 到 SI：超级智能体越强，方向越要在人手里](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-16-ai-to-si-super-agent.md) | 📌 看懂 AI Agent |
| 2026-10-15 | [AI 失忆不是 bug，是架构——记忆层补上了，然后呢？](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-15-ai-forgetfulness-is-architecture.md) | 📌 AI 工程化实战 |
| 2026-10-14 | [说不清需求，AI 就替你乱跑：Anthropic 工程师的原话，和我的三个解法](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-14-requirement-unclear-ai-runs-wild.md) | 📌 AI 工程化实战 |
| 2026-10-13 | [AI 写代码跑一半就'失忆'？把进度写成机器读得懂的文件](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-13-ai-coding-context-loss-sdd-v2.md) | 📌 AI 工程化实战 |
| 2026-10-12 | [AI 交叉对抗性审查：1 个模型，4 个专家，0 个额外账号](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-12-adversarial-review-4-experts.md) | 📌 AI 工程化实践 |
| 2026-10-11 | [AI 的记忆只有 30 天：你的对话正在被定时删掉](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-11-ai-memory-30-days.md) | 📌 AI 工程化实践 |

## 📚 分类索引

### 🔧 FDE · AI 工程化落地（13 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-17 | [写方案前，先让 10 个 AI 角色互怼](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-17-ai-roles-debate-before-plan.md) | 6 |
| 2026-09-28 | [一个 Skill 干所有事？我把它拆成了流水线](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-28-skill-pipeline-split.md) | 55 |
| 2026-09-25 | [FDE 工作法：进场、在场、离场，AI 落地是这样跑完的](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-25-fde-working-method-three-stages.md) | 134 |
| 2026-09-24 | [AI 越用越笨？问题不在模型，在上下文管理](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-24-token-09-context-management.md) | 30 |
| 2026-09-20 | [FDE 沟通三段论：拒绝需求但不拒绝人](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-20-fde-communication-three-step.md) | 9 |
| 2026-09-19 | [AI 工程师/FDE 招聘：会调 Prompt 不够，能去客户现场聊才是硬门槛](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-19-fde-hiring-client-site-communication.md) | 11 |
| 2026-09-18 | [小团队加 AI，一个多月交付十多万行代码：一次 FDE 实战复盘](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-18-small-team-ai-delivery-fde-review.md) | 75 |
| 2026-09-17 | [Palantir 的 FDE 拆成两个人：Echo 懂、Delta 造，AI 落地最后 100 米](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-17-palantir-fde-dual-role.md) | 105 |
| 2026-09-14 | [FDE 能力模型：8 个维度拆解，从技术到沟通的完整画像](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-14-fde-capability-model-8-dimensions.md) | 151 |
| 2026-09-13 | [untitled](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-13-pec-2026-conference-field-notes.md) | 207 |
| 2026-09-10 | [国家点名 FDE：AI 落地缺的不是模型，是现场的人](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-10-fde-ai-landing-people.md) | 180 |
| 2026-09-04 | [Vibe Coder、FDE、Harness Engineer……AI 时代的 5 种工程师，你是哪种？](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-04-five-types-engineers.md) | 11 |
| 2026-04-15 | [把4小时排查压到75分钟：我是如何用AI解决微服务'超卖'悬案的](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/04/2026-04-15-microservice-overselling-ai-troubleshooting.md) | 118 |

### 🚀 工具横评 · 模型实测（14 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-10 | [AI 编程贵，八成是浪费](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-10-ai-coding-half-is-waste.md) | 78 |
| 2026-09-23 | [Vibe coding 出来的代码没人看了：我花 spec 的时间比写代码还多](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-23-vibe-coding-nobody-reads-code.md) | 110 |
| 2026-09-22 | [省token横评：9个主流编程Agent谁最省token](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-22-token-benchmark-9-coding-agents.md) | 139 |
| 2026-09-21 | [我给 5 个 AI 工具写同一份说明书，两个月后 Claude Code 追上来了](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-21-five-ai-tools-same-spec.md) | 21 |
| 2026-09-16 | [员工比功能，老板看生态：WorkBuddy、豆包工作、千问办公选型账本](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-16-workbuddy-doubao-qwen-ecosystem-choice.md) | 173 |
| 2026-09-15 | [DeepSeek V4 Pro 不下线了：一场没完成的退役，和三个通用判断](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-15-deepseek-v4-pro-retirement-reversed.md) | 445 |
| 2026-09-12 | [DeepSeek 升级没让我改一行配置，我却删了 306 行规则](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-12-deepseek-upgrade-306-lines-removed.md) | 8 |
| 2026-09-11 | [DeepSeek 降价全景：旗舰砍到 1/7.5，企业只省 17.5%](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-11-deepseek-price-cutdown.md) | 23 |
| 2026-09-09 | [DeepSeek V4.1 Flash 内测上手：会看图了、快了 5.5 倍、价格一分没涨](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-09-deepseek-v4.1-flash-review.md) | 76 |
| 2026-09-08 | [AI Agent 到底是什么？三年，从会说话到会干活](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-08-ai-agent-explained.md) | - |
| 2026-09-07 | [Anthropic官方提示词手册：Fable 5.1的12条模式](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-07-fable-5.1-prompt-patterns.md) | 28 |
| 2026-09-05 | [GPT-6 Astra 与 Work Agent 时代，Harness 是工具还是规矩？——基于五级认知梯度的 AI 工程化可控性研究](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-05-harness-cognition.md) | 13 |
| 2026-08-28 | [省 token 的第一性原理：把「不用推理的活」，从模型手里拿回来](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/08/2026-08-28-save-token-first-principle.md) | 2 |
| 2026-08-27 | [智谱「牛来（Ox Alpha）」GLM-5.3 Flash 正式开源：输入 0.4 元 / 输出 1.4 元，比 DeepSeek V4 Flash 还便宜](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/08/2026-08-27-glm-5.3-flash.md) | 145 |

### 🌱 认知复利 · 方法论（1 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-09-06 | [为什么你做了很多事，却什么都没留下？——一套普通人也能用的知识复利方法](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-06-knowledge-compounding.md) | 51 |

### 📌 AI 原生组织 · 认知升级（1 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-09-29 | [AI 原生组织长什么样？没有岗位只有任务，普通人靠 high agency 保住竞争力](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/09/2026-09-29-ai-native-org-tasks-not-positions.md) | 35 |

### 📌 AI 工程化实践（4 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-20 | [我说了句「改吧」，AI 就不按规矩来了？](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-20-two-words-bypass-process.md) | 22 |
| 2026-10-19 | [你的 AI 护栏装了等于没装：三种静默失效](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-19-ai-guardrail-three-silent-failures.md) | 5 |
| 2026-10-12 | [AI 交叉对抗性审查：1 个模型，4 个专家，0 个额外账号](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-12-adversarial-review-4-experts.md) | 14 |
| 2026-10-11 | [AI 的记忆只有 30 天：你的对话正在被定时删掉](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-11-ai-memory-30-days.md) | 33 |

### 📌 AI 工程化实战（3 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-15 | [AI 失忆不是 bug，是架构——记忆层补上了，然后呢？](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-15-ai-forgetfulness-is-architecture.md) | 34 |
| 2026-10-14 | [说不清需求，AI 就替你乱跑：Anthropic 工程师的原话，和我的三个解法](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-14-requirement-unclear-ai-runs-wild.md) | 45 |
| 2026-10-13 | [AI 写代码跑一半就'失忆'？把进度写成机器读得懂的文件](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-13-ai-coding-context-loss-sdd-v2.md) | 50 |

### 📌 看懂 AI Agent（1 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-16 | [从 AI 到 SI：超级智能体越强，方向越要在人手里](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-16-ai-to-si-super-agent.md) | 28 |

### 📌 FDE实战（1 篇）

| 日期 | 标题 | 阅读 |
|------|------|------|
| 2026-10-21 | [项目范围越失控，客户越满意？一个 FDE 项目的真相](https://github.com/xingtu1996/xingtu-articles/blob/main/articles/2026/10/2026-10-21-project-scope-out-of-control-fde.md) | 3 |

## 🗂 按月归档

[2026-04（1 篇）](https://github.com/xingtu1996/xingtu-articles/tree/main/articles/2026/04) ｜ [2026-08（2 篇）](https://github.com/xingtu1996/xingtu-articles/tree/main/articles/2026/08) ｜ [2026-09（24 篇）](https://github.com/xingtu1996/xingtu-articles/tree/main/articles/2026/09) ｜ [2026-10（11 篇）](https://github.com/xingtu1996/xingtu-articles/tree/main/articles/2026/10)

---

## 关于作者 · 行途

- 公众号「行途 XingTu」（长文首发，微信搜索关注）
- GitHub / X：`@xingtu1996` ｜ 博客：https://xingtu1996.github.io
- 方法论旗舰仓：[xingtu-ai-engineering](https://github.com/xingtu1996/xingtu-ai-engineering)


## 📄 License

文章内容 [CC BY-SA 4.0](./LICENSE)；引用请注明「行途技术 · 公众号行途 XingTu」。
