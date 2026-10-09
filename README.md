# Khazix Skills

**中文** · [English](./README.en.md)

一组可直接被 Agent 加载的 [Agent Skills](https://agentskills.io)，遵循开放标准，Claude Code / Codex / OpenCode / OpenClaw 均可安装。

## 安装

在支持 Skill 的 Agent 里直接说：

```
帮我安装这个 skill：https://github.com/nowszhao/khazix-skills/tree/main/<skill-name>
```

把 `<skill-name>` 换成 `storage-analyzer`、`aihot`、`neat-freak`、`hv-analysis` 或 `khazix-writer`，Agent 会自行 clone 到对应目录。

## Skills

| Skill | 一句话 | 讲解 |
|---|---|---|
| [**storage-analyzer**](#storage-analyzer) | 扫描整机磁盘，三色分级给清理决策，网页上一键移废纸篓 | [公众号文章](https://mp.weixin.qq.com/s/NyOMIlOD986OC4SI9vmxlA) |
| [**aihot**](#aihot) | 一句话拿到 aihot.virxact.com 的每日 AI 日报与动态，无需 API Key | [aihot.virxact.com](https://aihot.virxact.com) |
| [**neat-freak**](#neat-freak) | 干完活跑 `/neat`，把本次改动与项目文档、CLAUDE.md、Agent 记忆对齐 | [公众号文章](https://mp.weixin.qq.com/s/tg1wd-iN2gWHWhXdY0faeg) |
| [**hv-analysis**](#hv-analysis) | 纵向追时间线 + 横向比同期竞品，产出万字 PDF 研究报告 | [公众号文章](https://mp.weixin.qq.com/s/Y_uRMYBmdLWUPnz_ac7jWA) |
| [**khazix-writer**](#khazix-writer) | 装上后 Agent 用「数字生命卡兹克」的口吻与节奏写长文 | [公众号文章](https://mp.weixin.qq.com/s/AtxGrii_K-nzkwUM9SNhEg) |

### storage-analyzer

扫一遍整机磁盘，在浏览器打开交互式 HTML 报告：磁盘总览、占用 Top 5、清理优先级、三色分级清单（🟢 纯缓存可一键清 / 🟡 含用户数据只给「在访达打开」「移废纸篓」/ 🔴 运行中应用与系统文件只解释不动）。每一项都给出具体路径、类型、删除影响与建议处置。全程只读扫描，删除必须点按钮 + 弹窗二次确认；本地服务跑在 127.0.0.1 + 随机端口 + token。macOS 完整实测，Windows 已支持多盘符。

触发：`帮我看看存储` · `C 盘满了` · `storage analysis`

### aihot

用中文一句话拉取 [aihot.virxact.com](https://aihot.virxact.com) 的 AI 日报：今日/指定日期日报、精选条目流、按分类（模型/产品/行业/论文/技巧）或时间窗口拉取、关键词与公司搜索。无需 API Key 或 MCP server。国内直连：

```bash
curl -fsSL https://aihot.virxact.com/aihot-skill/install.sh | bash
```

触发：`今天 AI 圈有什么新东西` · `最近一周的 AI 论文` · `最近 OpenAI 有什么发布`

### neat-freak

任务结束后运行 `/neat`，把本次会话改动与三层内容对齐：项目根的 `CLAUDE.md` / `AGENTS.md`、`docs/` 与 README、Agent 自己的记忆系统，最后给出变更摘要。解决「代码迭代七八轮、文档还是第一版」导致的 Agent 越用越笨。

触发：`/neat` · `整理一下` · `同步一下` · `sync up`

### hv-analysis

给一个产品 / 公司 / 概念 / 人物，同时跑两条线：纵向按时间讲完整演变，横向逐一对比同期主要竞品，交叉后输出 10,000-30,000 字的排版 PDF 报告。适合竞品调研、写作前期素材准备、从零搞懂一个领域；不适合查名词解释。

### khazix-writer

「数字生命卡兹克」的公众号写作 skill：完整风格规则（节奏、叙事、判断、修辞）+ 四层自检 + 风格示例库。它会**拒绝**「赋能、抓手、闭环」「首先…其次」「在当今 AI 快速发展的时代」这类表达。适合想要这个调子的长文写作，不适合追求通用好文笔的场景。

## License

MIT

Skill 原作者：[@KKKKhazix](https://github.com/KKKKhazix)（数字生命卡兹克）
