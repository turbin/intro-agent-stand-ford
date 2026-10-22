# CS329Z 讲义内容摘要

> 生成日期：2026-10-22 · 来源：`materials/papers/cs329z-slides/`（lecture01–09，共 9 份 PDF，约 120MB）
>
> 课程：**Stanford CS329Z: Engineering AI Agents**（Diyi Yang, Michael Ryan, John Yang，2026 秋）
> 课程主页：http://web.stanford.edu/class/cs329z

## 各讲摘要

### lecture01.pdf — Intro to Agentic Systems（71 页）

课程导论。内容包括：课程大纲与评分构成（项目 40%、作业 15%、测验 15% 等）；先修要求（CS 224N/224V/336 或同等 LLM 基础）；agent 思想史（1973 Actor 形式化 → 1980 Contract Net → 1990s 定义 → RL 时代 → LLM 时代）；agent 解剖图（LLM Core + Planning & Reasoning + Memory + Tools + Environment，源自 ReAct）；推理方法对比（CoT / Self-Consistency / Reflexion / 多 agent 辩论）；三类记忆（情景/语义/程序性）；复合 AI 系统（RAG 三步、工具调用四步、MCP）；五大挑战（可靠性、训练、长程、安全、评测）。

### lecture02.pdf — LLMs for Builders（176 页）

面向构建者的 LLM 原理课。定位在 LLM 技术栈最高层（应用层），但仍需理解底层：What is a Language Model、语言模型架构、训练、推理、LLMs for Agents 五部分。目标是理解现代 LLM 训练与推理的核心设计决策，以及这些决策带来的局限如何影响 agent 应用。

### lecture03.pdf — RAG + Agents（63 页）

检索增强生成。课程项目选题指导（选题标准、示例题目）；为什么需要 RAG；RAG pipeline 全流程；索引（chunking、contextual retrieval）；检索算法对比（BM25、DPR、ColBERT）；Agentic RAG（Self-RAG、Search-R1）；RAG 失败模式分析。

### lecture04.pdf — Tool Use（68 页）

工具使用。从 RAG 的四类问题引出工具的必要性（recall 天花板、lost in the middle、误差复合、prompt injection）；什么是工具；模型自学调用工具（Toolformer）；扩展到海量 API（Gorilla）；标准接口（REST、function calling、MCP）；工具使用评测基准（BFCL、ToolBench、τ-bench）。

### lecture05.pdf — Frameworks & Orchestration（132 页）

框架与编排。以 PyTorch 抽象 backprop 的类比引入"框架抽象掉系统细节"的思想；介绍 agent 工程常用框架及其抽象层；目标是把框架抽象与本课讨论过的底层系统设计对应起来，评估不同编排工具对 agent 可靠性的作用。

### lecture06.pdf — Agent Design Patterns and Scaffolds（86 页）

agent 设计模式与脚手架。引用 Martin Fowler"模式是半成品"说明需要按环境定制；定义 workflow 与 agent 的常见设计模式；对比不同上下文管理设计模式；剖析生产级 agent harness（如 Pi）中的设计决策。

### lecture07.pdf — Agent Memory Architectures（103 页）

agent 记忆架构。记忆对长期运行、多会话 agent 的必要性（以多会话邮箱助手为例）；agent 记忆的类型划分；几种具体的记忆架构实现；agent 记忆的开放挑战。

### lecture08.pdf — Multi-Agent Systems（92 页）

多智能体系统（MAS）。单 agent 与多 agent 系统的区分；MAS 编排模式；agent 间通信机制；协调基础设施与模式；MAS 的失败模式与挑战分析；案例研究（可选）。

### lecture09.pdf — Optimization（125 页）

优化。以 OPO 提示词实验（同一问题三种提示，PaLM 2 准确率 71.8%→80.2%）引入"用数据和评测表达意图并改进系统"；优化的适用条件；上下文优化（prompt 优化）与权重优化（微调）两类算法；agent 场景下的优化；如何选择优化策略。

## 配套笔记

- `notes/lecture01-预学习清单.md` — 第一课预学习清单（LLM 基础、必读论文、MCP 等，含优先级与学习顺序建议）

## 学习路线对照

第一课 P6 给出的课程结构：**Week 1–5 打基础**（lecture01–06 对应：导论、LLM、RAG、工具、框架、设计模式）→ **Week 5 之后进阶**（lecture07–09 对应：记忆、多 agent、优化；后续还有数据、评测、安全、coding agents、proactive agents 等）。
