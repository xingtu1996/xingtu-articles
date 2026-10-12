---
title: "AI 的记忆只有 30 天：你的对话正在被定时删掉"
date: 2026-10-11
slug: "ai-memory-30-days"
category: "AI 工程化实践"
summary: "Claude Code 默认 30 天清理本地会话，一行配置 cleanupPeriodDays 就能改成 10 年不过期。38 天攒下 17G token 的会话记录，这些没被清掉的东西才是真复利。"
---

# AI 的记忆只有 30 天：你的对话正在被定时删掉

先说结论：Claude Code 默认 30 天清理本地 session，一行配置 `cleanupPeriodDays: 3650` 就能改成 10 年不过期。你跟它聊过的每一句、每一次 bash 执行、每一次改错，都不是聊天记录，是未来能直接复用的资产。

## 1. 默认 30 天，你的对话正在被定时删

官方文档 `code.claude.com/docs/en/settings` 白纸黑字写了 `cleanupPeriodDays` 默认 30 天、最小 1。但它不是一打开就能看到的——它在 settings 文档的 hook-configuration 段，普通用户翻不到。

## 2. 38 天，我攒下了什么

我把清理周期改成 10 年后，38 天攒下 17G token 的会话记录。这些没被清掉的东西，才是真复利——它记录的不只是 prompt 和回复，还有每一次工具调用、每一次决策路径、每一次踩坑修正。

## 3. 为什么这事比调 prompt 重要

调 prompt 只影响单次输出质量；会话记忆决定的是你长期积累的资产量。AI 时代的复利，不在模型参数里，在你自己的历史会话里。
