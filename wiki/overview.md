---
title: "Overview"
type: synthesis
tags: [agent, RAG, retrieval, filesystem, proactive, context, understanding, harness, knowledge]
sources: [agent-everything-is-file, agent-proactive-context-economics, ai-tools-access-vs-understanding, harness-knowledge-moat]
last_updated: 2026-05-05
---

# Overview

*This page is maintained by the LLM. It is updated on every ingest to reflect the current synthesis across all sources.*

## Current Knowledge Base

本知识库目前聚焦于 **AI Agent 架构、交互模式与认知模式**的演进。

### 核心主题

**Agent 认知模式的分化：访问 vs 理解**
- 访问（Access）：给 AI 接入所有工具，2025年行业已解决
- 理解（Understanding）：综合、消解矛盾、建立统一认知，几乎没人在做
- 检索模式是"寻宝游戏"：每次从零开始，没有先验理解，没有积累
- 理解模式是持续更新的现实模型：答案在被问前就已存在
- MCP 是更好的检索管道，但没有解决理解问题

**Agent 交互模式的分化**
- 被动式 Agent（ChatGPT、Claude、Gemini）正在逼近天花板，能力维度越来越同质化
- Coding Agent（Claude Code、Cursor）率先突破，采用"主动看代码、主动建议、主动执行"方式
- 主动式桌面 Agent 正在探索通用场景，核心是改造"模型与人的协作方式"而非让模型更聪明

**人类注意力窗口的经济学**
- 模型 context window 在扩张，但人类的 Human Context Window 固定且有限
- 这一矛盾导致意图大规模遗漏、任务大规模断点
- 主动式 Agent 通过捕获意图闭环信号（如 Enter 键）解决多线程工作中的任务遗漏
- 未来 90% 的 context 将发生在人与 AI 之间，而非人与人之间

**RAG 检索方法的演进**
- 传统向量检索在跨页面查询和精确匹配场景下存在局限性
- 新一代方法通过让 Agent 使用熟悉的工具接口（如 POSIX 命令）来提升检索精度
- 检索不应局限于向量搜索，可以是全文搜索、SQL 查询、文件系统操作等任何方式

**Agent 工具设计哲学**
- LLM 对训练数据中高频出现的接口（如 shell 命令）理解更深
- 复用已有接口优于创造新工具：文件系统是 Agent 的"母语"
- 工具组合能力（管道、链式调用）是 POSIX 工具链的核心优势

**虚拟文件系统架构**
- ChromaFS 案例展示了如何将数据库伪装成文件系统
- 通过命令拦截和翻译，实现零学习成本的 Agent 交互
- 适用于结构清晰、读多写少的文档场景

### 关键洞察

**意图捕获的信噪比**
- 全量截图记录的是"这个人在场"，噪音太大
- Enter 键记录的是"这个人在做选择"，是构成意图轨迹的最小有效单元
- Enter 之前是私密的思考流，Enter 之后是对外的承诺

**组织协作的范式转变**
- 人类两千年来依赖层级制，因为"人同时只能管理 3-5 人/Agent"
- AI 时代可能打破这一限制，让 context 在团队内充分流转
- Agent 应归属员工而非公司，以项目/群组形式协作并选择性分享 context

**复利式理解：真正的护城河**
- 理解会随时间积累并产生复利效应，每个新数据点都让现有图谱更有价值
- 理解必须积累，不能加速，不能用钱跳过
- 今天开始的公司，六个月后会拥有六个月的复利理解，这是以后砸多少钱都追不上的
- 真正的护城河不是技术（可以被复制），而是公司对自身的积累理解
- AI 的真正机会：第一次让理解从人脑迁移到系统，变成可持续的资产

**Harness Engineering：工作流是管道，知识是活水**
- Harness Engineering 强调引导和约束 AI 模型能力，而非提升模型本身
- 三支柱：上下文工程（知识检索注入、长/短期记忆）、架构约束（Agent 编排）、持续治理（知识生命周期）
- 知识管理本身就是 Harness Engineering 的核心能力，而不是附属品
- 工作流会迭代更新（状态机 → DAG），但领域知识是永恒的
- 知识是"可累积的"复利资产，工作流是"可替换的"管道

**知识分层架构**
- 五层存储：Layer 0-P（个人偏好）→ 0-T（团队约定）→ 1（技术知识）→ 2（业务知识）→ 3（项目知识）
- 五种类型：model（实体定义）、decision（技术选型）、guideline（推荐做法）、pitfall（已知风险）、process（业务流程）
- 三级成熟度：draft → verified → proven，长期不被引用会自动衰减
- 三级渐进式索引：全景目录（~50行）→ 分类清单（~300行）→ 完整条目（按需），上下文效率提升一个数量级
- 知识可以"向上提升"：项目知识 → 技术知识/业务知识
