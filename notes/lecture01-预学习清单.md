# CS329Z 第一课《Intro to Agentic Systems》预学习清单

> 来源：lecture01.pdf（71 页）。第一课本身是导论，不深入展开，但通篇默认你已掌握以下基础。

## 一、课程官方前置要求（Page 12，明确写了"本课不讲"）

- **先修课**：CS 224N（NLP）/ CS 224V / CS 336（LLM 从零构建）或同等水平
- **必备 LLM 概念**（讲师明确说默认你会）：
  - train / dev / test set（训练/验证/测试集）
  - pretraining（预训练）
  - fine-tuning（微调）
  - alignment（对齐）
  - prompting（提示工程）

## 二、LLM 基础中的重点

| 主题 | 为什么需要 | 优先级 |
|---|---|---|
| **In-context learning（上下文学习）** | 第一课把 GPT-3 的 ICL 定为"LLM 时代的开端" | ⭐ 必看 |
| **Context window 限制** | 讲课直接用它引出"为什么 agent 需要 Memory"（Page 45） | ⭐ 必看 |
| **CoT（Chain-of-Thought, Wei et al. 2022）** | Page 35–37 直接对比 Standard / CoT / ReAct 三种推理方式 | ⭐ 必看 |
| **采样与解码概念** | 理解 tool call 中 constrained decoding（Page 58）需要 | 了解即可 |

## 三、第一课引用的核心论文（按重要性排序）

| # | 论文 | 出现在 | 讲什么 | 优先级 |
|---|---|---|---|---|
| 1 | **ReAct**（Yao et al., 2022） | P25/29/36–37 | Reason+Act 交替范式，全课的"agent 解剖图"就来自它 | ⭐⭐ 必读 |
| 2 | **Reflexion**（Shinn et al., 2023） | P39–40 | 用自然语言自我反思改进决策 | ⭐ 必读 |
| 3 | **Self-Consistency**（Wang et al., 2023） | P38 | 多条推理路径投票聚合 | ⭐ 必读 |
| 4 | **Generative Agents**（Park et al., 2023） | P45–47 | 情景记忆（episodic memory）的经典实现 | ⭐ 必读 |
| 5 | **Toolformer**（Schick et al., 2023） | P51 | LLM 自学何时/如何调用 API | ⭐ 必读 |
| 6 | **Voyager**（Wang et al., 2023） | P46/49 | 程序性记忆（以代码形式存技能） | 推荐 |
| 7 | **Multi-agent debate**（Du et al., 2023） | P41–42 | 多智能体辩论提升推理 | 推荐 |
| 8 | **Gorilla**（Patil et al., 2023） | P52 | LLM 连接海量 API | 推荐 |
| 9 | **MRKL Systems**（2022） | P24 | 模块化推理+工具调用的早期工作 | 了解即可 |
| 10 | **Magentic-One**（Microsoft, 2024） | P43 | Orchestrator 协调多 agent | 了解即可 |

## 四、强化学习背景（Agent 历史 RL 时代，P22）

- **Agent-Environment Loop**（Sutton & Barto《Reinforcement Learning: An Introduction》第 3 章）——第一课的 act/observe 循环图直接沿用这个框架 ⭐
- DQN 玩 Atari（Mnih et al., 2015）——了解"agent 概念在 RL 时代的样子"即可

## 五、复合 AI 系统与工具生态（P54–59）

- **Compound AI Systems** 博客（Zaharia et al., BAIR 2024）——"Workflow vs Agent"的分界：代码定步骤 vs LLM 定步骤 ⭐
- **RAG 三步流程**：Retrieve → Augment → Generate（P57）
- **Tool use 调用四步**：Select → Arguments → Validate → Execute（P58）
- **MCP（Model Context Protocol）**：官方文档 https://modelcontextprotocol.io ——课程后续会大量用到 ⭐

## 六、推荐的课外导读（补充背景）

- **Lilian Weng 博客**《LLM Powered Autonomous Agents》(2023)——第一课 P31 直接引用她的 agent 定义
- Agent 思想史（P19–21，听懂即可）：Contract Net Protocol（1980）、Minsky《Society of Mind》（1986）、Wooldridge & Jennings 的 agent 四特征（autonomy / social ability / reactivity / proactivity）
- **HAL 评测平台**：https://hal.cs.princeton.edu ——课程讲 reliability gap 时反复用（P62–63）

## 建议学习顺序（约 1–2 天）

1. LLM 基础自查：ICL、CoT、context window（半天）
2. 精读 ReAct（1–2 小时）——整个课程的地基
3. 读 BAIR Compound AI Systems 博客 + Lilian Weng 博客（1 小时）
4. 浏览 MCP 官方文档 Quickstart（1 小时）
5. 其余论文按上表优先级扫读 abstract + 图
