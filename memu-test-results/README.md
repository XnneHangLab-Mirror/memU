# memU recall test results

memU codex 适配器的记忆召回测试（codex-cli 0.144.5 / grok-4.5 中转 · Ollama
`bge-m3` · 隔离测试库，真实用户库从未写入）。**两组实验，数据严格分开，勿混用：**

## 组 1 — per-session baseline（逐个会话组）
每个 case 独立：自己的 Session A → `prepare` → 挖掘 → `commit` → 自己的 Session B。
记忆随 case 逐步累积、被补丁加厚（7 → 7.5 → 11 是同一条记忆的完整生命周期）。

- 用例规范：`recall-testcases.md`（正式版，中文）· `recall-cases-extended.md`（简单格式扩展稿）
- 报告（EN）：`case7-reading-mishima.md` · `case7.5-reading-isao.md` · `case8-gaming-skyrim.md`
  （更早的 case4/case5 EN 报告已移出本目录）
- 报告（CN）：`case7-cn-…` `case7.5-cn-…` `case8-cn-…` `case9-cn-…` `case9.5-cn-…`
  `case10-cn-…` `case11-cn-…`
- **记忆数据：`cn-store/`** —— 中文 baseline 跑完后的真实末态库：
  `memory/*.md`（由 `memu-codex prepare` 从库中重新生成，非手抄）、
  `memu-test-cn.sqlite3`（完整向量库）、`config.env`（key 为 placeholder）、
  `list-files.txt`。末态 = 经过 7.5/9.5/11 补丁后的 5 条记忆。

## 组 2 — once-talk experiment（一次性混合会话组）
对照实验：同一批事实（三岛/村上/天际两点/Chill with You）塞进**一次对话的一条
消息**，一次 prepare、一次挖掘、**一次 commit**，全新空库。探测语与组 1 完全相同。

- 报告：`exp-once-talk-cn.md`（含与 baseline 的逐探测对比表）
- **记忆数据：`once-store/`** —— 同样由 memU 自己 mirror 导出：`memory/*.md`
  （5 条，明显比 cn-store 版本更瘦）、`memu-test-once.sqlite3`、`config.env`、
  `list-files.txt`。
- 结论：功能 4/4 PASS，但「今晚想放松」探测的文件级排名反转（天际 0.6005 >
  chill 0.5982；baseline 为 chill +0.109 领先），周末约束在回答中被软化——
  逐会话渐进积累提供的「语义厚度」是模糊探测区分度的直接来源。

## 快速对照
| | 组 1 per-session | 组 2 once-talk |
|---|---|---|
| 会话数 | 每 case 独立 A/B（7 个 case） | 1 个 A + 4 个探测 B |
| commit 次数 | 每 case 一次 | 全部一次 |
| 库 | `cn-store/`（记忆被补丁加厚） | `once-store/`（一次性瘦记忆） |
| 结果 | 10/10 PASS，约束干净 | 4/4 PASS，P9 排名反转+约束软化 |
