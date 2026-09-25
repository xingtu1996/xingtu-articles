---
title: Vibe coding 出来的代码没人看了：我花 spec 的时间比写代码还多
tags: [Vibe Coding, spec, Harness, 工程思想, AI 编程]
original: https://mp.weixin.qq.com/s/y3YHTQlthtrT6fbE-UZfaQ
views: 68
category: AI工程化实战
author: 行途
---
【配图：00-引子图-vibe-coding.png】

# Vibe coding 出来的代码没人看了：我花 spec 的时间比写代码还多

> 我用 Claude Code 跑了 239 亿 token、10.8 万次请求之后，发现一个反直觉的事实：AI 写代码越快，人对齐 spec 的时间反而越多。

---

## 一、一个群里的真实对话

昨天在一个开源交流群里，有人问了一个问题：

> "现在大家 vibe coding 出来的代码已经完全不看了吗？"

下面有人回答：

> "不怎么画原型图了，大部分直接出 demo。"
> "三个月后不知道会进化成什么样子。"
> "我是看不过来，所以前面对齐 spec 和验收标准会花更久。"

这三句话，说出了 vibe coding 时代的真实困境。

---

## 二、什么是 vibe coding？

2025 年 2 月，OpenAI 联创 Karpathy 发了一条推文，提出了"vibe coding"这个词：

> "fully give in to the vibes, embrace exponentials, and forget that the code even exists."
> （完全跟随感觉，拥抱指数级增长，忘记代码的存在。）

他的做法是：
- 用 Cursor Composer + Claude Sonnet
- 几乎不碰键盘
- 点"Accept All"不看 diff
- 把错误信息复制粘贴回去让 AI 修

这条推文 400 万浏览，"vibe coding"成了 2025 年度词汇（柯林斯词典）。

---

## 三、8 个月后：hangover 来了

但仅仅 8 个月后，2025 年 9 月，Fast Company 就宣布"vibe coding hangover"来了。

发生了什么？

**1. 45% 的 AI 生成代码有缺陷**
不是小问题，是安全漏洞、性能问题、逻辑错误。

**2. Lovable 事件：170 个应用数据泄露**
一个叫 Lovable 的 AI 编程平台，生成的 170 个应用全部存在数据泄露问题。

**3. 高级工程师说"development hell"**
代码写出来了，但没人看得懂，也没人敢改。你不知道 AI 到底写了什么。

到 2026 年，"vibe coding"这个词已经分裂成三种意思：

| 版本 | 定义 | 用途 |
|---|---|---|
| 原始版 | 不看代码，只看能不能跑 | 原型、demo |
| 漂移版 | 任何 AI 辅助开发 | 什么都往上套 |
| 贬义版 | 直接上生产没验证 | 技术债、安全风险 |

Andrew Ng 在 2025 年 6 月公开批评：**"vibe coding 是一种危险的幻觉。"**


【配图：04-UncleBob_不看代码_Twitter对话.jpg】
---


【配图：01-vibe-coding时间线.png】
## 四、我的真实实践：从 vibe 到 spec


【配图：05-xingtu-sdd仓库.png】
我用 Claude Code + CC Switch 跑了 4 个月，10.8 万次请求，239 亿 token。

**前两个月**：确实是 vibe coding——描述需求，AI 写代码，能跑就行。

**第三个月开始**：发现不对了。

- 代码能跑，但没人看得懂
- 改一个功能，要重新让 AI 读一遍整个项目
- 出了 bug，不知道是 AI 写错了还是我描述错了

**现在我的做法**：

### 1. 多 story 并行：多会话窗口 + worktree

我现在同时跑 3-5 个 Claude Code 会话窗口，每个窗口负责一个 story。用 git worktree 隔离代码，互不干扰。

依赖服务？提前 mock 掉，不让 AI 卡在环境问题上。

### 2. 单 epic 复杂：sub-spec 分解降维

一个大 epic（比如"重构整个用户系统"），我不会直接让 AI 写。

我会先拆成 sub-spec：
- sub-spec 1：用户表结构设计
- sub-spec 2：登录接口改造
- sub-spec 3：权限系统重构
- sub-spec 4：测试用例补全

每个 sub-spec 单独一个会话，写完验收，再进下一个。


【配图：02-spec实践三步.png】
### 3. 上下文管理：该 compact 就 compact，该 clear 就 clear

这是最重要的一条。

**该 compact 的时候就 compact**——上下文太长了，AI 开始胡说八道，压缩一下。

**该 clear 的时候就 clear**——一个 story 做完了，不要让 AI 带着包袱进下一个 story。放弃包袱，让 agent 和你重新开始，梳理思路再基于既有的 spec 资产，重新开始做工作续接。

---

### 4. 我的 SDD 方法论：从 vibe 到"签合同"

这半年踩坑踩多了，我自己整理了一套 SDD（Spec-Driven Development）方法论，开源在 GitHub 上：`xingtu1996/xingtu-sdd`。

核心就一句话：**跟 AI 干活前先签一份"合同"（规格），写清要什么、怎么验收；AI 照做，做完拿合同逐条验收。**

业界现在流行的 spec 方案（比如 GitHub 的 spec-kit）是**命令驱动**的——你要记 8-19 个命令，敲 `/speckit.specify`、`/speckit.plan`，人去适应工具。

我做的 xingtu-sdd 走**意图路由**——你说人话就行："按 specs 标准推进这个功能"，AI 自己判断深浅、自动走流程。工具适应人，不是人适应工具。

还有一个关键区别：**深度可裁**。单文件 bug 轻量 2 个文件就够，架构改造才需要全量流程。不是所有事情都要写一大堆 spec——小事轻装，大事重型。

这套方法从 40+ 真实工程里蒸馏出来，去掉了业务绑定，任何项目都能用。仓库地址放文末了，感兴趣可以看看。

---

## 五、Harness：把 AI 装进受控轨道


【配图：03-Harness六层架构.png】
我在工作区里搭了一套 Harness（AI 自媒体操作系统），核心就是把"人对齐 spec"这个环节固化下来。

**六层架构**：
- L5 产品层：HARNESS.md（愿景/路线图/进化机制）
- L4 编排层：workflows/（内容生产/发布/开源/复盘）
- L3 执行层：agents/ + skills/（10个专业Agent + 技能SOP）
- L2 护栏层：rules/ + specs/（规则 + 规格驱动）
- L1 土壤层：config/ + tools/（配置 + 工具）
- L0 记忆层：memory/（沉淀/复盘/经验）

**核心思路**：AI 写代码很快，但人对齐 spec 很慢。那就把"对齐 spec"这个环节从对话里固化成文件，让 AI 每次都读同一份 spec，而不是每次都重新描述一遍。

---

## 六、最核心的一句话

**认知和思想不能交出去。**

AI 没有目的，人得把控方向。

让工具成为工具，让人成为人。

---

