# WORDY

> A tiny daily word workout.

**WORDY** 是一个极简、纯前端的英语近义词 / 反义词配对消除小游戏：每天 5 关，用几分钟练习词汇关系、拼写和语感。

## Highlights

- **One-file app**：全部 HTML、CSS、JavaScript 集成在 `index.html`，无需构建、后端或 API。
- **Daily Seed**：使用当前日期 `YYYY-MM-DD` 生成 deterministic seed，所有玩家每天获得同一组题目。
- **Difficulty ladder**：Level 1–2 使用基础词汇，Level 3–4 使用 GRE / TOEFL 常用与学术词汇，Level 5 使用高阶词汇；每天刷新一套新题。
- **No same-day repeats**：同一天的 5 个关卡从统一的每日计划中抽题，跨关卡不重复出现相同词对或词汇。
- **Challenge History**：完成每日 5 关后，在本机日历中标记完成日期，并记录当天分数与用时；无需账号或后端。
- **Wrong answer book**：配对失败或 Meaning Lab 答错时，自动保存错词、英文释义、例句、错误次数与最近日期，集中复习且只保存在当前浏览器。
- **Expanded vocabulary**：加入 `adversity / alleviate / arbitrary / bolster / conspicuous / deter / eclectic / exacerbate / pragmatic / scrutinize / sporadic / tenacious` 等 GRE / TOEFL 核心词及同反义关系。
- **Meaning Lab**：独立的每日词义辨析模式，使用四选一情境题区分近义词的语义边界，并在作答后给出即时解析。
- **Responsive mobile layout**：针对手机宽度优化双列卡片、缩小间距、题目选项、顶部栏、统计卡与结算弹窗，支持 480px 以下窄屏。
- **Dark Mode**：顶部一键切换 Light / Dark，自动读取系统偏好，并使用 `localStorage` 记住用户选择。
- **Game feel**：选中高亮、匹配缩放、错误 Shake、Combo 连击与计时挑战。
- **Learn while playing**：配对成功显示词汇关系与简明释义；点击卡片使用 Web Speech API 播放英文发音。
- **Local-first progress**：`localStorage` 保存 Streak、最高分、历史完成日历、主题偏好与今日通关状态，不上传任何数据。
- **GitHub Pages ready**：直接上传 `index.html` 即可发布。

## Run locally

```bash
# Option 1: double-click index.html
# Option 2: serve it locally for a more realistic browser preview
python3 -m http.server 8080
```

然后访问 <http://localhost:8080>。

## Deploy to GitHub Pages

1. 创建一个 GitHub repository。
2. 上传 `index.html`（以及本 README）。
3. 在 **Settings → Pages** 中选择 `Deploy from a branch`。
4. 选择默认分支的根目录并保存。

## Tech

- Semantic HTML
- Modern CSS with a small custom design system
- Vanilla JavaScript
- Tailwind CSS CDN（仅用于少量布局与 utility class）
- Web Speech API
- `localStorage`
- CSS media queries + theme tokens

## Note

词汇释义与辨析说明为适合游戏阅读的简明学习型内容，参考 Cambridge / OED 风格进行整理；本项目不依赖在线词典 API，因此可离线运行（Tailwind CDN 已缓存或不可用时，核心自定义 CSS 仍可工作）。历史记录保存在当前浏览器中，清除网站数据或更换设备后不会同步。
