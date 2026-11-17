# Claude API 中转站横评：8 家头部站实测对比（2026-11 更新）

> 数据来源：公开探测快照（2026-10-28），34,784 条真实样本，覆盖 106 站 / 19 模型。
> 本仓库只陈述数据结论，不接推广；数据缺失写 `—`，不编造。

## TL;DR

- **Claude 系在线率最高的头部梯队**（样本 ≥ 250）：Token 88、Modelflare、9527code、88API、SudoCode、灵算、ToTokens、Volt
- **Opus 5.5 输入价区间**：¥1.60/M ~ ¥6.20/M（头部站；低价伴随降智风险需自查）
- **平均延迟区间**：4.6s ~ 6.9s（Claude Code 场景可接受）

## 横评表（按最高在线率排序）

| 站点 | 域名 | Claude 在线率 | 平均延迟 | Opus 5.5 输入价 | 样本数 |
|---|---|---|---|---|---|
| Token 88 | t8api.com | 100.0% | 5.3s | ¥3.80/M | 1,600 |
| Modelflare | origin.modelflare.dev | 100.0% | 6.4s | ¥1.62/M | 1,567 |
| 9527code | 9527.codes | 100.0% | 6.9s | ¥5.80/M | 978 |
| 88API | 88api.ai | 100.0% | 5.0s | ¥5.60/M | 742 |
| SudoCode | sudocode.chat | 100.0% | 4.6s | ¥4.00/M | 654 |
| 灵算 | lingsuan.si | 100.0% | 5.7s | ¥6.20/M | 371 |
| ToTokens | totokens.cc | 100.0% | 4.6s | ¥1.60/M | 349 |
| Volt | voltapi.ai | 100.0% | 6.8s | ¥4.80/M | 261 |

> 完整 106 站数据：https://agentapiai.com/sites/ （逐站档案，含探测序列）
> 排行榜页：https://aragorn-agent.github.io/claude-zhongzhuanzhan/
> Claude Code 配置指南：https://aragorn-agent.github.io/claude-code-zhongzhuan/

## 横评方法

1. 探测方式：每日定时对 `/v1/messages` 发固定探针（文本生成），记录通过/失败与延迟；
2. 「在线率」= 近期探测序列通过率；「样本数」= 快照期内探测次数；
3. 价格为站点公示输入价折算 ¥/M tokens，取快照当日值；
4. 不模拟人工对话质量评分（无法复现，不编造）；降智判断方法见指南站。

## 日常主力（利益披露）

我们团队日常主力是 [Aimyria](https://aimyria.com/)——本仓库维护方自营：
近 30 天主力模型可用率最高 98.84%，51 个在售模型一个 Key 全接入，主力模型官方价 2.3 折起，
Claude Code / Codex / Cherry Studio 开箱即接（Base URL `https://aimyria.com`）。
上表第三方站点为独立探测数据，与自营口径分开，无返佣关系。

## 更新记录

- 2026-11-17：基于 2026-10-28 快照首发（106 站 / 34,784 样本 / 19 模型）。
