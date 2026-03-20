# xhs-content-ops-skill

小红书内容运营包装 Skill 合集。

这个仓库收录用于小红书内容发布优化的 Claude Skill，基于真实导出数据分析提炼而来，脱敏后公开，供其他创作者参考、修改、复用。

---

## 这个仓库是什么

不是教你怎么写内容的地方，是**发布前最后一公里**的工具集：

- 分析竞品导出数据，找赛道规律
- 优化标题、封面文案、首屏钩子
- 埋搜索关键词
- 判断发布形式（图文 / 视频 / 双发）

适用于：选题已定，或草稿已有，需要做发布包装的场景。

---

## 目录结构

```
xhs-content-ops-skill/
├── README.md                        ← 你在这里
├── skills/
│   └── xhs-ops-optimizer/          ← 第一个 skill：运营包装优化
│       ├── SKILL.md                 ← Skill 主文件（给 Claude 读的）
│       └── references/             ← 参考资料库
│           ├── benchmark-insights.md
│           ├── keyword-clusters.md
│           ├── platform-rules.md
│           └── title-formulas.md
└── data/
    └── xhs数据导出-0320/            ← 原始数据与分析报告（已脱敏）
        ├── *.csv                    ← 小红书导出的搜索词样本数据
        ├── 小红书AI赛道爆款分析报告-260320.md
        ├── 小红书AI赛道深度运营洞察-260320.md
        └── 小红书流量与运营机制调研-260320.md
```

---

## Skill 列表

| Skill | 说明 |
|---|---|
| `xhs-ops-optimizer` | 小红书内容运营包装优化，含数据分析、标题优化、关键词埋点、发布形式判断 |

后续会持续补充其他 xhs 相关 skill。

---

## 数据来源说明

`data/xhs数据导出-0320/` 里的原始数据来自 2026 年 3 月 20 日对小红书 AI 赛道的批量搜索词导出，涵盖的关键词包括：

- AI 教学、AI 产品、AI 入门、AI 分享、AI 开发
- agent、claude code、cursor、mcp、vibe coding、skill
- 文科生学 AI、低粉爆文筛选

所有文件已脱敏（移除了账号 ID），分析报告中不含个人账号数据。

---

## 怎么用这个 Skill

### 方式一：直接复制 SKILL.md 给 Claude

把 `skills/xhs-ops-optimizer/SKILL.md` 的内容粘贴到你的 Claude 对话开头，或者放进你的 Claude 项目 Instructions。告诉 Claude 你有什么（CSV 数据 / 草稿 / 选题），它会按流程走。

### 方式二：安装到 Claude Code 的 .claude/skills/

如果你在用 Claude Code，把 `skills/xhs-ops-optimizer/` 整个文件夹复制到你项目的 `.claude/skills/` 目录下，就可以用 `/xhs-ops-optimizer` 触发。

### 方式三：基于原始数据自己重新分析

`data/` 里的 CSV 是原始导出样本，你可以：

1. 用 Claude 直接分析这些 CSV，看看哪些内容在跑
2. 根据你自己的赛道导出新的数据，替换掉这些 CSV
3. 基于分析结果重新修改 `references/` 里的参考文件，生成你自己领域的 Skill

---

## 修改建议

references 里的四个文件是 Skill 的知识底座，可以直接按你自己的赛道改：

- `benchmark-insights.md`：换成你的赛道样本规律
- `keyword-clusters.md`：换成你的目标关键词
- `platform-rules.md`：补充你观察到的最新平台规则
- `title-formulas.md`：加入你自己总结的有效标题结构
