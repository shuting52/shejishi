---
name: "clay_design_showcase"
description: "黏土风 UI 设计 Skill（v7）：真·视觉 DNA v4（可爱 3D 黏土风＋弥散渐变＋引导页 coach mark＋性别选择 8 版式＋集卡骨架＋付费订阅 8 版式＋关键词筛选 7 版式＋底部TAB 7 套图标＋卡片设计 8 版式，来自用户提供的 92 张正文截图实测 + 3 个通用组件）＋ ① 31 个通用组件的设计 Prompt 库，每个可直接投喂 AI 设计工具出稿；② 14 套风格变量（黏土/国潮/暗黑霓虹/极简奶油/复古港风/新拟态/手绘风/Bento格栅/液态玻璃/新丑风/千禧复兴/多巴胺/瑞士大字报/扁平插画，每套配完整 token 表）；③ 代码桥接：设计稿一键转可运行单文件 HTML；④ 设计验收环：10 项自检＋打回重做；⑤ 项目全案模式；⑥ v7 新增：设计师视角（选用决策树+反模式+点评模式）/ 组件六态矩阵 / 自动化流水线（输入项目名→8 步自动出全套，scripts/scaffold.py 一键脚手架）；⑥ 6 种黏土风封面版式一键提示词卡 + 万能总提示词。版式结构按用户提供的设计参考 1:1 复刻，角色与文案用原创替换，绝不复制任何第三方原稿。"
---

# 黏土风设计 Skill（v7）

## Purpose
一套"从创意到整套 App 设计稿再到可运行代码"的提示词资产：输入任意创意或一个完整项目，输出可直接投喂 AI 设计工具的 Prompt，并附黏土风封面物料，方便做设计或做内容。v6 补齐三口气：**多风格**（[14 套风格变量](references/style-variants.md)，一套组件十四种味道）、**代码桥接**（[设计稿转可运行 HTML](references/code-bridge.md)）、**验收环**（[10 项自检清单](references/design-qa.md)＋打回重做）。v7 再补四口气：**懂设计师**（[设计师视角](references/design-principles.md)：组件选用决策树＋风格选用指南＋10 条反模式＋点评话术）、**风格做深**（每套风格配完整 token 表：颜色/圆角/阴影/字体/动效，直接落地代码）、**状态补全**（[组件六态矩阵](references/component-states.md)：28+3 组件的默认/选中/禁用/空/加载/错误必备态）、**自动化**（[自动化流水线](references/auto-pipeline.md)：输入项目名→品类识别→风格推荐→主题表→IA→组件映射→逐屏 Prompt→封面→验收→代码，8 步自动跑；`scripts/scaffold.py` 一键生成 pack 骨架）。新增第三批样图实测：性别选择 8 版式、集卡活动骨架（见 [visual-dna.md](references/visual-dna.md) 第三批）。用户会持续提供设计参考截图，按"版式结构 1:1 复刻、角色文案原创替换"原则持续写入。

## 三种使用模式
- **模式 A｜单组件设计**：用户说"设计一个XX组件"→ 从 [组件 Prompt 库](references/component-prompts.md) 取对应卡片，填主题变量后交付 UI 生成提示词。
- **模式 B｜黏土风内容**：用户说"用黏土风做一条XX"→ 走 v2 的 3 问交互，交付标题+封面提示词+正文+标签（见下方交互模式）。
- **模式 C｜项目全案**：用户输入一个项目（如"房屋出租"）→ 按 [项目全案模式](references/project-mode.md) 输出：项目定位 → 主题规范 → 信息架构 → 逐屏设计 Prompt → 黏土风封面系列。

输入判断：含"App/项目/做一款"等词 → 模式 C；含"黏土风/设计赏析"→ 模式 B；只提单个组件 → 模式 A。
只给项目名（如"打车"）→ 走 v7 自动化流水线：先跑 `python3 scripts/scaffold.py "{项目名}"` 生成骨架，再按骨架填血肉。

## 自动化流水线（v7，模式 C 的自动挡）
见 [auto-pipeline.md](references/auto-pipeline.md)。8 步：品类识别 → 风格推荐 → 主题表 → IA → 组件映射 → 逐屏 Prompt（拼风格 token 行 + 状态句式）→ 封面 → 验收 → 代码。已在"闪乘打车"项目验证跑通。

## 交互模式（模式 B，3 问即出）
1. 做哪个组件/主题？（给 3 个推荐，也可自由输入）
2. 用哪种封面版式？（A 标准干货 / B 横排变体 / C 原创改版 / D 配色特辑 / E 产品渲染 / F IP实验，默认 A）
3. 署名写什么？（提醒换成用户自己的）
问完直接出四件套，不再追问。也可把 [万能总提示词](references/master-prompt.md) 整段贴给任何 AI，它会自动按此流程交互。

## Workflow（模式 C 项目全案）
1. **定主题。** App 名 + slogan + 风格（14 套风格变量选一，见 [style-variants.md](references/style-variants.md)）+ 主色/深色/背景色 + 圆角/字体 + 3 个风格关键词，写入主题变量表。
2. **画 IA。** 输出信息架构树：Tab 结构 + 核心页面 + 弹窗 + 活动。
3. **列清单。** 每个页面/组件映射到组件库编号，项目特有页面单独写 Prompt。
4. **逐屏出 Prompt。** 每个屏幕一份完整 UI 生成提示词（风格 token + 主题变量已填入）+ 推荐封面卡 + 黏土风标题。
5. **过验收。** 按 [设计验收环](references/design-qa.md) 10 项自检，不通过打回重做。
6. **出代码。** 按 [代码桥接](references/code-bridge.md) 把每屏转成可运行单文件 HTML + index.html 原型目录。
7. **打包。** 输出 `project-pack.md`（主题表 + IA + 逐屏 Prompt 清单 + 代码文件清单）。

## Output Contract
- 模式 A：`component-prompt.txt`（UI 生成提示词）+ 可选封面四件套
- 模式 B：`title.txt` + `cover-prompt.txt` + `body.md` + `tags.txt`
- 模式 C：`project-pack.md`（主题变量表 / IA 树 / 逐屏 UI Prompt / 逐屏封面 Prompt / 黏土风系列标题清单）

## Operating Rules
1. **版式结构按用户提供的设计参考 1:1 复刻；角色形象与文案用原创替换**，不复制任何第三方及 IP 的原稿、原图、原文案；组件名是通用词汇，可以用。
2. 所有 UI 生成提示词默认：先选风格（14 套风格变量，token 表见 [style-variants.md](references/style-variants.md)，默认黏土可爱）+ 竖屏手机 9:19.5、中文界面、写明主色/圆角/字体变量；末尾必须加状态句式（必备态查 [component-states.md](references/component-states.md)）。
3. 黄色关键词色值锁死 #FFD400（仅封面）。
4. 中文大标题字生图易错：提示词注明"标题字后期叠加"。
5. 截图矩阵用真实 App 截图拼贴，不让 AI 编造假界面。
6. 标 [待用户补] 的细节不编造。
7. 用户语言优先，默认中文输出。
8. 完整示例：[单组件示例](references/worked-example.md) / [项目全案示例·房屋出租](references/project-example-house-rental.md) / [项目全案示例·今天吃什么](references/project-example-what-to-eat.md) / [项目全案示例·扫码点餐小程序](references/project-example-food-order-miniprogram.md) / [项目全案示例·社区团购小程序](references/project-example-groupbuy-miniprogram.md)，先看示例再开工。做小程序项目必读 [小程序适配清单](references/miniprogram-notes.md)（无启动页/图标、避让胶囊、订阅消息）。

## Style Source（置信度）
- 已采样（2026-10-15）：公开渠道可见的 12 条设计笔记标题与封面视觉，拆出 6 种封面版式。
- 用户提供 15 张正文截图 [实测]：第一批 5 张（启动图标/租房筛选/引导页/黏土输入法）→ 可爱 3D 黏土风 DNA；第二批 10 张（弥散渐变配色卡/引导页 coach mark/启动图标黄红蓝三系/启动页矩阵）→ 渐变体系与引导页语言。样图存于 references/samples/。
- 未采样：其余 20 条笔记正文/话题（登录墙）。组件库中的通用设计规范为行业通用写法，非其独家内容。
