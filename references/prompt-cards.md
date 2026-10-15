# 一键提示词卡（6 种版式）

每张卡都是"复制→替换占位符→投喂生图模型"即用。占位符：`{关键词}`=组件名，`{署名}`=你的署名。
通用后期提醒：中文大标题建议用设计工具叠加，生图只负责底版+矩阵排版。

---

## 卡片 A：标准干货封面 [实测]（最常用）

适用：`💥设计赏析｜X` / `💥设计参考｜X` 系列。样本中 7 条用此版式。

中文说明：UI 干货笔记封面，纯黑背景。左上白色描边空心胶囊"设计细节"（或"案例分享"），右上白色小字"-UI/UX"。中央大标题：白色粗黑体"设计赏析-" + 明黄色大字"{关键词}"。下方 2 列 4 行共 8 张手机截图拼贴，圆角卡片，全是"{关键词}"相关界面。底部中央小字署名"{署名}"。大字报风格，高对比。

English prompt（复制投喂）：
```
Xiaohongshu UI design showcase cover, pure black background #000000, vertical 3:4.
Top-left: small white outline pill badge, white Chinese text "设计细节".
Top-right: small white text "-UI/UX".
Center: bold headline, white Chinese characters "设计赏析-" followed by large bright yellow #FFD400 Chinese characters "{关键词}".
Lower half: 2-column x 4-row grid of 8 rounded-corner smartphone app screenshots, all showing {关键词} interfaces, neat collage.
Bottom center: tiny white watermark "{署名}".
Style: bold poster typography, high contrast, clean flat UI, no people, no other text.
Negative prompt: blurry, low contrast, wrong Chinese characters, extra captions, photorealistic people, gradient background.
```

填例：{关键词}=搜索历史，{署名}=独立设计师

---

## 卡片 B：横排变体封面 [实测]

适用：截图是横版海报/贴片类的主题（如直播贴片）。

与 A 的区别：标题下方是**横向一排 4 张**宽截图；左下角署名"{署名}"，右下角一枚小彩色 logo。

English prompt：
```
Xiaohongshu UI design showcase cover, pure black background #000000, vertical 3:4.
Top-left: white outline pill badge "案例分享". Top-right: small white text "-UI/UX".
Center headline: white "设计赏析-" + bright yellow #FFD400 "{关键词}".
Below headline: ONE horizontal row of 4 wide app screenshots showing {关键词}, edge to edge.
Bottom-left: small white text "{署名}". Bottom-right: small colorful abstract logo mark.
Bold poster typography, high contrast, no people.
Negative prompt: blurry, wrong Chinese characters, extra text, gradient background.
```

---

## 卡片 C：原创改版项目封面 [实测]（置顶门面用）

适用：完整的 App/小程序改版案例。浅色底，与干货系列形成反差。

中文说明：米白浅色背景。左上角深色实心胶囊"置顶"。中央巨大粗黑体概念词"{概念词}"，下方副标题"{项目名}体验改版原创设计"。2~3 台手机 mockup 斜放，展示改版后的界面。右上角小字水印"@{署名}"。干净高级。

English prompt：
```
Premium app redesign showcase cover, warm light beige background #F5F1E8, vertical 3:4.
Top-left: dark solid pill badge with white Chinese text "置顶".
Center: huge bold black Chinese characters "{概念词}", subtitle below "{项目名}体验改版原创设计".
2-3 smartphone mockups floating at slight angles, screens showing the redesigned {项目名} UI.
Top-right: small watermark "@{署名}".
Style: clean, premium, minimal, generous white space, no people.
Negative prompt: dark background, cluttered, wrong Chinese characters.
```

填例：{概念词}=有里，{项目名}=游浙里

---

## 卡片 D：配色/材质特辑封面 [实测，已按她的弥散渐变卡校准]

适用：渐变、配色、材质等视觉主题。

中文说明（实测还原）：纯黑背景。左上白字"UI设计-配色篇"，右上灰色小字"-UI/UX"。中央一张深色圆角大卡片（近乎黑），卡片顶部斜插一张双层"标签纸"（白+ pastel 色）。卡内：手写体 "Hello!"（白色）+ 大号粗黑体中文主题词（如"弥散渐变"）。卡片下半部分是 aurora 弥散渐变（从底部向上晕染：橙黄 / 蓝紫 / 粉紫 / 青绿四选一）。底部 3 个白描边色圆 + hex 标注。2-3 条极细白色弧线点缀。

English prompt：
```
UI color palette showcase cover, pure black background #000000, vertical 3:4.
Top-left: white bold Chinese text "UI设计-配色篇". Top-right: small gray text "-UI/UX".
Center: one large dark rounded card (near-black #0A0A0A), a double-layer paper tag (white + pastel) tucked diagonally at its top edge.
Inside card: white handwritten script "Hello!" at top, huge bold white Chinese characters "{主题词}" in center.
Lower half of card: aurora mesh gradient blooming upward ({渐变描述}, e.g. orange-yellow / blue-purple / pink-purple / teal-green).
Bottom: 3 white-outlined color dots with hex codes below them.
2-3 ultra-thin white curved lines as decoration.
Style: premium, glowing gradients on black, minimal.
Negative prompt: flat colors only, blurry, wrong text, cluttered.
```

填例：{主题词}=弥散渐变，{渐变描述}=orange-yellow aurora

---

## 卡片 E：产品渲染教程封面 [实测]

适用：Figma/工具教程、玻璃拟态等单品深度教程。

中文说明：深海军黑背景。左上小字英文 "LIQUID GLASS"（字母间距拉开）。中央大标题白字+浅蓝字"{主题}"。一只产品大渲染图（如智能手表）占据视觉中心，展示玻璃拟态"{组件}"效果。极简高级。

English prompt：
```
UI tutorial cover, deep navy-black background #050810, vertical 3:4.
Top-left: small letter-spaced uppercase English text "LIQUID GLASS".
Center: large title, white + light blue Chinese text "{主题}".
Hero: one large 3D product render (smartwatch style) showing glassmorphism {组件} UI, purple-blue glass tones, soft glow.
Minimal, premium, lots of dark negative space, no people.
Negative prompt: cluttered, bright background, wrong text.
```

---

## 卡片 F：IP/视觉实验封面 [推测·低频]

适用：原创 IP、插画、手绘风作品。刻意跳出黑底公式，一年只做少量。

中文说明：全幅彩色渐变背景（如红粉渐变）。顶部白色立体大字"{IP名}"，下方手写体中文名。中央一个原创吉祥物插画（{形象描述}，如"戴耳机踩滑板的番茄"）。俏皮、有记忆点。

English prompt：
```
Original IP character showcase cover, full-bleed vibrant gradient background (red to pink), vertical 3:4.
Top: huge white 3D bubble letters "{IP名}", handwritten-style Chinese name below it.
Center: original mascot illustration, {形象描述}, playful cartoon style, dynamic pose.
Fun, bold, memorable. No UI screenshots.
Negative prompt: dark background, realistic photo, generic stock character.
```

---

## 通用负面清单（所有卡片可追加）
```
watermark (other than specified), logo soup, distorted hands, extra fingers,
mismatched fonts, low resolution, jpeg artifacts
```
