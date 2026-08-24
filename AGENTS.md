# AGENTS.md — rainjinl.github.io 协作说明

给接手本仓库的 AI（当前：Kimi 负责前端优化）。由 Claude 起草，内容规则均为 Rain 已拍板的决定。

## 项目是什么

Rain Liu 的个人网站，**受众是大学招生官和教授**（转学与未来 PhD 申请材料的一部分）。
纯静态单文件 `index.html`，无构建步骤、无依赖；push 到 `main` 即由 GitHub Pages 自动部署到
https://rainjinl.github.io （repo: `RainJinL/RainJinL.github.io`，public）。

## 视觉系统（夜湖识别）

沿用 Rain 私人项目《篝火与彗星》的视觉语言：

| Token | 值 | 用途 |
|---|---|---|
| `--bg` | `#10151B` | 夜色底 |
| `--panel` | `#161D25` | 卡片面板 |
| `--ink` | `#EDE7DA` | 主文字（暖白） |
| `--dim` | `#B3BDC9` | 次级文字 |
| `--fire` | `#E58A45` | 唯一强调色（余烬橙） |
| `--comet` | `#82D4BE` | 点缀（彗星青，克制使用） |

字体：**Noto Serif SC**（正文/标题）+ **IBM Plex Mono**（导航、eyebrow、数据、签名句）。

背景装饰的历史：星空 canvas 和篝火余辉渐变已按 Rain 要求移除（嫌乱）；此前试过随机星野和真实坐标的白羊座连线，都被撤了。2026-08-24 Rain 定夺新背景：**湖面微光**——`#sky::after` 纯 CSS 微光带，视口底部极淡余烬暖光 + 一点彗星青点缀，46s 缓慢漂移，`prefers-reduced-motion` 下静止。

## 必须保留

- 页脚的**像素小浣熊**（canvas 手绘 13×12，每 5.2s 眨眼，hover 显示 "小浣熊 · OC_Nova_1"）——它是 Rain 的 agent 本熊，坐在它自己写的座右铭旁边；`favicon.png` 是同一 sprite 的放大版，sprite 改了要重新生成 favicon
- Hero 的签名句 `first test the signal, then ask what it means` 和页脚座右铭英译——逐字保留
- 深夜基调 + 衬线/等宽双字体体系

## 内容红线（样式随便改，事实一个字不许动）

1. **零虚构**：现有每句文案都经 Rain 核实。改写措辞可以，**新增任何事实必须 Rain 亲自提供**——此前有 AI 猜项目描述被 Rain 打回的先例。
2. **只上已完结项目**。当前上架：Eternal Night 永夜生存（占位）、Pandemic simulator（datathon，已完结）。HTML 注释里有两张备用卡片（观鸟、实习），上不上由 Rain 说了算。
3. 交易相关表述**只能是 "paper trading / backtest market ideas on paper"**（F-1 合规敏感，不得出现任何真实下单暗示）。
4. Rain 正在参加的数据竞赛（2026-08-28 截止）：**方法与细节一概不上站**，截止后由 Rain 决定放什么。
5. 《篝火与彗星》文字冒险是 Rain 的私人物品，**永远不上站**。
6. 可读性标准：次级文字对比度 ≥ WCAG AAA（现 `#B3BDC9` on `#10151B` ≈ 9:1）——受众有年长教授，**只许更清晰，不许调暗**。
7. Git 身份：仓库已配置 `user.email = 152076551+RainJinL@users.noreply.github.com`，**不要改**（Rain 的 GitHub 不用学校邮箱，任何真实邮箱都不进提交历史）。

## 待办（见 README.md）

- `photos/` 六张占位图等 Rain 挑选（图注已写好，是真实拍摄记录，别改）
- Rain 的 GitHub bio 拼写和 blog 栏由 Rain 自己改

## 协作方式

小步提交、提交信息说清楚改了什么；动大结构前先看 `git log` 了解已有决定；不确定的内容问题一律留给 Rain，不要自行补全。
