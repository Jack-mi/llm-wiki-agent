# Wiki Log

Append-only chronological record of all operations.

Format: `## [YYYY-MM-DD] <operation> | <title>`

Parse recent entries: `grep "^## \[" wiki/log.md | tail -10`

---

## [2026-05-05] ingest | Agent：一切皆文件

摄入了关于 Mintlify ChromaFS 虚拟文件系统的技术文章。

**创建的页面：**
- 源文档：`sources/agent-everything-is-file.md`
- 实体：`Mintlify.md`, `ClaudeCode.md`, `OpenViking.md`
- 概念：`ChromaFS.md`, `RAG.md`, `VectorRetrieval.md`

**核心主题：**
- RAG 检索方法从向量搜索向 Agent 自主工具使用的演进
- 文件系统作为 Agent "母语"的设计哲学
- 虚拟文件系统架构在文档检索场景的应用

**无矛盾发现**（这是知识库的第一篇源文档）
## [2026-05-05] ingest | Agent 的第一性问题：Proactive 与 Context 经济学

摄入了五源资本对 AirJelly 创始人黄柏特的访谈文章。

**创建的页面：**
- 源文档：`sources/agent-proactive-context-economics.md`
- 实体：`AirJelly.md`, `黄柏特.md`, `五源资本.md`, `Cursor.md`
- 概念：`ProactiveAgent.md`, `HumanContextWindow.md`, `NextEnterPrediction.md`, `CodingAgent.md`
- 更新：`ClaudeCode.md`（添加主动式交互特性）

**核心主题：**
- 主动式 Agent 与被动式 Agent 的本质区别
- 人类注意力窗口（Human Context Window）的固定性与模型 context window 扩张的矛盾
- Enter 键作为意图闭环最小单元的设计哲学
- Coding Agent 率先突破被动响应边界
- 组织协作范式在 AI 时代的潜在变革

**与现有内容的关系：**
- 与 [[agent-everything-is-file]] 形成互补：
  - 前者关注 Agent 的工具接口设计（文件系统作为"母语"）
  - 本文关注 Agent 的交互模式设计（主动式 vs 被动式）
- 两篇文章共同构建了 Agent 设计的两个维度：工具层（what）和交互层（how）

**无矛盾发现**
## [2026-05-05] ingest | 工具接了几十个，AI 还是搞不懂你的公司

摄入了 Hyperspell 联合创始人 Conor Brennan-Burke 关于 AI Agent 从"访问"到"理解"的深度文章。

**创建的页面：**
- 源文档：`sources/ai-tools-access-vs-understanding.md`
- 实体：`Hyperspell.md`, `ConorBrennanBurke.md`
- 概念：`ContextGraph.md`, `AccessVsUnderstanding.md`, `CompoundingUnderstanding.md`, `MCP.md`

**核心主题：**
- 访问（Access）vs 理解（Understanding）的本质区别
- 检索模式的五大缺陷：矛盾无处不在、同一对象多个标识、信息会腐烂、来源有权重差异、需要跨源综合
- Context Graph（上下文图谱）：持续更新的公司现实表示
- 复利式理解：真正的护城河，不能加速、不能用钱跳过
- 文件系统作为通用输出接口，让上下文与 Agent 供应商解耦
- MCP 是更好的检索管道，但没有解决理解问题

**与现有内容的关系：**
- 与 [[agent-everything-is-file]] 都认同文件系统是 Agent 的通用接口
- 与 [[agent-proactive-context-economics]] 形成互补：
  - 前者关注交互模式（主动 vs 被动）
  - 本文关注认知模式（检索 vs 理解）
- 三篇文章共同构建了 Agent 设计的三个维度：工具层（what）、交互层（how）、认知层（understand）

**无矛盾发现**
## [2026-05-05] ingest | Harness不是目的，知识才是护城河

摄入了腾讯 AI Team 工程交付团队关于 Harness Engineering 与知识沉淀的实践文章。

**创建的页面：**
- 源文档：`sources/harness-knowledge-moat.md`
- 实体：`AITeam.md`, `Karpathy.md`, `Codex.md`
- 概念：`HarnessEngineering.md`, `KnowledgeLayering.md`

**核心主题：**
- Harness Engineering 的本质：引导和约束 AI 模型能力，而非提升模型本身
- 工作流是管道，知识是活水：工作流会迭代更新，但领域知识是永恒的
- 知识分层架构：五层存储 × 五种类型 × 三级成熟度
- 三级渐进式索引：全景目录 → 分类清单 → 完整条目，上下文效率提升一个数量级
- 知识的三通道沉淀：冷启动导入、每次需求、自动引用追踪闭环
- 文件系统即状态机：所有状态、产物、知识都以文件形式存在
- 远程操控能力：突破人机交互瓶颈，让工作流 7×24 小时流转

**与现有内容的关系：**
- 与 [[ai-tools-access-vs-understanding]] 的 [[CompoundingUnderstanding]] 概念完全一致
- 与 [[agent-everything-is-file]] 的文件系统哲学一致（文件系统即状态机）
- 与 [[agent-proactive-context-economics]] 形成互补：前者关注交互模式，本文关注知识沉淀
- 四篇文章共同构建了 Agent 工程的完整视图：
  - 工具层（what）：文件系统作为通用接口
  - 交互层（how）：主动式 vs 被动式
  - 认知层（understand）：检索 vs 理解
  - 知识层（accumulate）：知识分层与沉淀

**无矛盾发现**
