# xingtu-cloud-neutral · 云中立 / Agent 中立理念层

> 主张并实证「资产归你、格式通用、可随工具迁徙」的工作方式：技能、自动化、数据沉淀在本地文件 + 跨工具事实标准上，工具是耗材，资产是自己的。
> 本仓是理念正本；配套盘点技能落在 [xingtu-skills](https://github.com/xingtu1996/xingtu-skills)，定时任务定义落在 [xingtu-scheduled](https://github.com/xingtu1996/xingtu-scheduled)，每周盘点台账在 `inventory/`。

## 一句话

**云中立 = 资产归你、格式通用、可随工具迁徙的工作方式。**

## 背景：一个人的工具带

2026 年的现实：一个重度 AI 用户机器上同时存在 20+ 个 AI 工具，每个工具都有自己的 skills 目录、会话格式、配置体系。工具在洗牌（Claude Code / Codex / Gemini / Grok / 豆包 / ZCode / WorkBuddy / Trae / Cursor…），模型在换代，云在涨价。此时只有两种活法：

1. **绑定式**：把工作流锁进某一云 / 某一工具——工具换代即资产清零，且持续交租（订阅、额度、迁移成本）。
2. **云中立式**：把技能、自动化、数据沉淀在**本地文件 + 跨工具事实标准**上——工具是耗材，资产是自己的。

本仓主张并实证第二种。

## 三条纪律（可执行，不是口号）

### ① 资产可导出

一切落在本地文件系统：Markdown / JSON / HTML。

- 禁把核心资产锁进任何云端专有数据库（可用，但必须本地有导出件）。
- 单文件、零依赖、离线可用——十年后还能打开。
- 每周台账可 diff，增量对比工具矩阵与漂移。

### ② 格式跨工具

遵循 `SKILL.md` 事实标准（`name + description + when_to_use` frontmatter + Markdown 正文）：

- 这是 Claude Code / CodeBuddy / Codex / Cursor / Gemini CLI / DSH 等共同消费的格式。
- 一份技能发布一次，所有工具可用（渐进式披露：索引常驻 + 按需读全文）。
- 自动化同样工具中立：定义用 YAML 落仓（`automations/`），可在任何平台重建。

### ③ 换工具不换资产

- 新工具出现 → 只做「安装指向」，资产原地不动。
- 工具停服 → 资产无损，技能 / 数据原样迁到下一个工具。
- 判定标准：**换掉任何一个工具，一周内能否恢复全部工作流？** 能，才是云中立。

## 目录结构

| 路径 | 内容 |
|---|---|
| `docs/cloud-neutral.md` | 理念正本（README 只做摘要，冲突以本文件为准） |
| `inventory/` | 每周盘点产出：机器可读台账 JSON + 单文件 HTML 看板 |
| `automations/` | 每周盘点定时任务定义（平台侧按它重建） |

## 与隐私的关系

云中立的前提是**资产干净**：公开产出只含聚合数字与泛化路径。配套技能内置 30 词脱敏红线表（身份 / 雇主代号 / 凭据类目录名），0 命中才落盘。

## 反模式（云中立不背的锅）

- ❌ 为了中立而自虐：该用的云服务照用，只是**核心资产不留锁**。
- ❌ 把「中立」当不付费：商业工具该订订，中立指的是**可迁徙**，不是白嫖。
- ❌ 格式洁癖：事实标准优先，完美格式不如现在能跑。

## 与聚合仓的关系

- 盘点技能：[xingtu-skills](https://github.com/xingtu1996/xingtu-skills)（toolbelt-scan 工具带扫描技能）。
- 定时任务：[xingtu-scheduled](https://github.com/xingtu1996/xingtu-scheduled)（多 Agent 定时任务 registry）。
- 工程脚本：[xingtu-tools](https://github.com/xingtu1996/xingtu-tools)（本机脚本工具集）。

## 关于作者 · 行途 XingTu

- 公众号「行途技术手记」：微信搜索关注，看 AI 工程化落地实战。
- GitHub：[@xingtu1996](https://github.com/xingtu1996)
- 方法论旗舰仓：[xingtu-ai-engineering](https://github.com/xingtu1996/xingtu-ai-engineering)

## License

MIT License。
