# xingtu-cloud-neutral · 云中立 AI 工具带

> **不绑定任何云、任何厂商、任何工具。**
> 你的技能、自动化与数据，归你所有——换工具不换资产。

[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE) ![Cloud Neutral](https://img.shields.io/badge/cloud--neutral-no--vendor--lock--in-blue.svg) ![Tools](https://img.shields.io/badge/tools-25-blue.svg) ![Skill Installs](https://img.shields.io/badge/skill%20installs-284-orange.svg)

---

## 这是什么

一个 AI 工程化实践者的**本机 AI 生态实证仓**。这里没有框架、没有 SDK、没有"某云专属"——

只有一条被真实验证的工作方式：

- 一台机器上同时跑着 **25 个 AI 工具**（Claude Code / Codex / Gemini / Grok / WorkBuddy / CodeBuddy / ZCode / DSH / 豆包 / 千问 / Cursor / Trae / Qoder / Lingma / Junie / OpenCode / Antigravity…）
- **283 次技能安装**、去重后 **111 个技能**、**17.1 GB** 工具数据
- 全部资产用**跨工具事实标准**（SKILL.md：`name + description + when_to_use`）沉淀
- 一份发布，到处运行——这就是云中立。

本仓记录这套生态的**每周盘点**（`inventory/`）与**理念 SSoT**（`docs/`），
技能本体在姊妹仓 [xingtu-skills](https://github.com/xingtu1996/xingtu-skills)（127 个生产级技能）。

## 为什么是"云中立"

模型在涨价、工具在换代、厂商在洗牌。把工作流锁死在任何单一云/工具上，
都是在用自己的资产给别人交租。云中立 = 三条可执行的纪律：

| 纪律 | 做法 | 本仓实证 |
|---|---|---|
| **资产可导出** | 一切落在本地文件（md/json/html），不锁进任何云端数据库 | 17.1GB 工具数据全部本地可迁 |
| **格式跨工具** | 遵循 SKILL.md 事实标准，一份技能 Claude/Codex/Gemini/豆包全可用 | 111 个去重技能跨 25 工具安装 |
| **换工具不换资产** | 工具是耗材，技能/自动化/数据是资产 | 见 `docs/cloud-neutral.md` |

## 仓结构

```
xingtu-cloud-neutral/
├── README.md                  ← 你在看的（门面）
├── docs/
│   └── cloud-neutral.md       ← 理念 SSoT（为什么 + 怎么做）
├── automations/
│   └── toolbelt-weekly-scan.yaml  ← 每周盘点的工具中立自动化定义
├── inventory/                 ← 每周盘点产出（由定时任务喂）
│   ├── toolbelt_inventory.json    ← 机器可读台账（增量对比基准）
│   └── 2026-10-12.html            ← 首期盘点看板
└── LICENSE                    ← MIT
```

## 每周盘点怎么跑

1. 技能 `toolbelt-scan`（SSoT 在 [xingtu-skills](https://github.com/xingtu1996/xingtu-skills)）只读扫描全机 AI 工具
2. 产出 JSON 台账 + 单文件 HTML 看板，落入本仓 `inventory/`
3. 与上周增量对比：新工具 / 技能变动 / 版本漂移 / 僵尸技能 / 数据增长
4. 任何输出先过 30 词脱敏红线表（0 命中才落盘）——**公开的只有聚合数字与泛化路径**

想在本地复现：

```bash
# 装技能（跨工具通用）
git clone https://github.com/xingtu1996/xingtu-skills.git
cp -r xingtu-skills/skills/toolbelt-scan ~/.claude/skills/   # 或 ~/.codex/skills/ 等任意工具

# 跑盘点
python3 ~/.claude/skills/toolbelt-scan/scripts/toolbelt_scan.py
```

## 首期快照（2026-10-12）

| 指标 | 值 |
|---|---|
| 检测到 AI 工具 | 25 |
| 技能安装总次数 | 284 |
| 去重后技能 | 112 |
| 跨工具同名技能 | 43（其中 23 个存在版本漂移） |
| 僵尸技能（无 SKILL.md） | 4 |
| 工具数据总量 | 17.1 GB |

完整矩阵与漂移榜见 [`inventory/2026-10-12.html`](inventory/2026-10-12.html)。

## 和行途开源矩阵的关系

本仓是**数据/理念层**，不管技能生产。技能、工具、文章各仓：

| 仓 | 层 | 干什么 |
|---|---|---|
| [xingtu-skills](https://github.com/xingtu1996/xingtu-skills) | 技能 | 127 个跨工具 SKILL.md |
| [xingtu-ai-engineering](https://github.com/xingtu1996/xingtu-ai-engineering) | 方法论 | AI 工程化文章 |
| [harness-kit](https://github.com/xingtu1996/harness-kit) | 工具 | AI 工作台生成器 |
| [md2wechat](https://github.com/xingtu1996/md2wechat) / [book2vido](https://github.com/xingtu1996/book2vido) / [article2pod](https://github.com/xingtu1996/article2pod) | 工具 | 内容生产管线 |

矩阵导航：[github.com/xingtu1996](https://github.com/xingtu1996)

---

一线 AI 工程化实践者 · FDE 方向 · 公众号「行途」（长文首发）· GitHub/X：`@xingtu1996`

*本仓所有盘点输出均为聚合数字与泛化路径；从不包含任何个人身份信息、凭据或雇主内部信息。*
