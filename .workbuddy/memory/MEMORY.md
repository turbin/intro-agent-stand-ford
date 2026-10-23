# 项目长期记忆

## 项目概况
- 主题：CS329Z（Engineering AI Agents，Diyi Yang 等，2026 秋，Stanford）第一课预学习 + MBA 论文工作区（paper-rsi-harness 结构）。
- 规则：materials/ 原件只读；变更后跑 `python3 .paper-ai/paper.py index --root . --reason <说明>` 更新索引。

## 进行中
- **待续问答（下次会话主动提示用户）**：`tasks/lecture01-ReAct-稀疏想法-待续问答.md` —— ReAct「稀疏想法引导长程规划」苏格拉底对话，Q4 已抛出待答（ReAct-IM 密集想法为何反而有害）。纪要见 `notes/lecture01-ReAct-稀疏想法-苏格拉底问答.md`。
- 第一课阅读材料 14 份在 `materials/papers/lecture01-reading/`（优先级清单：`notes/lecture01-预学习清单.md`）。

## 已完成
- 2026-10-22：ReAct 全文中文译稿 `notes/ReAct_全文翻译.html`（A4 版式，自包含，33 页原文图像内嵌）；图 1/4/5 图内文字系 CID 偏移乱码，用 +0x1D 解码脚本还原（脚本在 `tmp/2026-10-22/decode_figtext.py`）。
- 2026-10-23：ReAct 实验设计详细分析（同源消融、刻意弱化检索器、200 例人工失败模式分析、防守性设计），已口头输出并配 3 张图。
