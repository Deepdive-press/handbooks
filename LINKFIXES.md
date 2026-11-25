# 死链修复台账 · LINKFIXES

> 2026-11-25 外链巡检修复记录。背景：全站 4555 条外链程序化审计报告 35 条 404；
> 逐条二次核实（服务端抓取 + 搜索引擎交叉验证）后确认死链 12 条、误报存活 21 条、
> 反爬/JS 壳无法程序化判定 2 条（保留原链）。本台账只登记确认死链的处理结果。

## 处理结果（12 条确认死链）

| # | 原链接（404） | 处理 | 新链接 / 替代来源 | 命中手册 |
| --- | --- | --- | --- | --- |
| 1 | plausible.io/blog/one-blog-post-traction | 迁移 | plausible.io/blog/blog-post-changed-my-startup | AI 生态市场手册 |
| 2 | chainlight.io/post/curve-finance-analysis-and-post-mortem | 原文已下线+替代 | Hacken：Curve 流动性池攻击事件剖析 | 链上数据分析手册 |
| 3 | code.claude.com/docs/en/create-a-marketplace | 迁移 | code.claude.com/docs/en/plugin-marketplaces | AI 生态市场手册 |
| 4 | docs.langchain.com/langsmith/evaluate-agent-intermediate-steps | 迁移 | docs.langchain.com/langsmith/evaluate-on-intermediate-steps | AI 生态市场手册 |
| 5 | github.com/hop-protocol/airdrop | 仓库改名 | github.com/hop-protocol/hop-airdrop | 链上数据分析手册 |
| 6 | handbook.gitlab.com/.../all-remote/effective-communication/ | 原文已删除+替代 | handbook.gitlab.com/handbook/communication/ | AI 时代个人效率系统手册 |
| 7 | openai.com/api/scale-tier/ | 迁移 | openai.com/api-scale-tier/ | AIAgent 自动化变现手册 |
| 8 | alchemy.com/faucets/ethereum | 产品收缩 | alchemy.com/faucets/ethereum-sepolia | Web3 安全实操手册、Web3 赚钱手册 |
| 9 | arduino.cc/en/main/FAQ | 改版迁移 | support.arduino.cc/hc/en-us | 桌面工厂变现手册 |
| 10 | cnbc.com/2023/03/11/stablecoin-usdc-breaks-dollar-peg... | 原文已删无存档+替代 | 美联储 FEDS Notes：SVB 挤兑与稳定币影响 | 链上数据分析手册 |
| 11 | coinspeaker.com/mev-bot-12m-loon-20-profit | 原 slug 拼写错误 | coinspeaker.com/mev-bot-12m-loan-20-profit/ | Web3 赚钱手册 |
| 12 | support.tastytrade.com/.../Kalshi-Event-Constracts | 原 slug 拼写错误 | support.tastytrade.com/.../Kalshi-Event-Contracts | 预测市场与信息金融手册 |

## 审计误报说明（21 条 ALIVE + 2 条 BLOCKED，未改动）

- FTC（consumer.ftc.gov）×4：对中国大陆 IP 全站返回 404，服务端与搜索引擎均证实存活。
- wallstreetcn.com ×4、CGC（cards.cgccards.cn / cgccards.com）×3：实测 200 且内容吻合。
- n8n 社区帖、金标尺、IT之家、PolymarketIndex、伯克利信息安全、Arctic7、闲鱼创作者平台等：WAF 对简单客户端返回假 404。
- data.stats.gov.cn 与 econpapers.repec.org：实测完整返回（审计标注「疑似拒爬」经复核不成立）。
- drops.scamsniffer.io（反爬墙，Wayback 证实存活）、douyin 视频页（JS 壳）：无法程序化判定，保留原链。

## 修复纪律

1. ALIVE 一律不动；无法判定不标死；新 URL 必须验证 200 且主题吻合后才替换。
2. 原文下线的保留原 URL 为文字标注「来源原文已下线（检索日期）」+ 补替代来源。
3. 同步修复范围：仓库书页 + 本地 fragments / chapters / 成书（防重装配复发）。
