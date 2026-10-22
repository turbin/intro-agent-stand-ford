# MBA 论文工作目录

运行 `.paper-ai/paper.py --help` 查看命令。原始材料放 materials/，先把本轮允许提供给模型的文本清单写到任务 brief。
更改写作主题（如“我想改一版xxx主题的内容”）使用 `.paper-ai/paper.py reset-topic --topic <新主题>`：先不加 --confirm 生成计划与备份提交，确认后再加 --confirm 执行清空重建。
未实现 PDF 自动解析；请先人工核对并转为 notes/ 下的 Markdown，保留原始页码。
索引用 index 命令或 PM 运行自动更新，不是实时文件监听器。
