# 项目全案示例：美食决策 App《今天吃什么》

输入："做一个叫'今天吃什么'的 App" → 模式 C 完整输出。

## 主题变量表
| 变量 | 值 |
|---|---|
| App 名 | 今天吃什么 |
| slogan | 别纠结，吃就对了 |
| {主色} | #FF4D2E 番茄红 |
| {深色} | #1A1D21 炭黑 |
| {背景色} | #FFF9F5 暖米白 |
| 点缀色 | #FFC531 芥末黄 |
| {圆角} | 16px 卡片 / 12px 按钮 / 全圆角胶囊 |
| 风格关键词 | 美食大图、食欲感、转盘随机、年轻化 |

## IA 树
```
今天吃什么
├─ 启动页 → 首页
├─ Tab：首页 / 发现 / 消息 / 我的
│  ├─ 首页：搜索栏、跑马灯（今日推荐）、"今天吃什么"转盘入口、分类 chips、附近美食卡片流
│  ├─ 发现：美食笔记/菜谱流
│  ├─ 消息：拼单/约饭会话
│  └─ 我的：个人主页、积分签到、吃货会员、设置
├─ 随机决定页（大转盘 / 灵魂三问）
├─ 搜索页 / 筛选页
├─ 餐厅详情页 / 菜谱详情页
├─ 弹窗：筛选底部弹窗、分享底部弹窗、更新弹窗
└─ 活动：集美食卡赢霸王餐
```

## 逐屏 Prompt 清单

### S1 启动页 [库01]
```
Mobile app splash screen "今天吃什么", 9:19.5. Background gradient #FF4D2E to #1A1D21, subtle grain.
Center: white geometric logo (bowl + question mark merged), soft glow.
Below: bold white "今天吃什么", slogan "别纠结，吃就对了" in 70% white.
Bottom tiny text "v1.0.0". Appetizing, clean, no photo.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·启动页`

### S2 启动图标 [库02]
```
App icon, rounded square. Solid #FF4D2E background, subtle top highlight.
Center: bold white glyph, rice bowl with a question mark as steam, geometric, no text.
Recognizable at small size. Show on light + dark backgrounds.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·启动图标`

### S3 首页（定制：转盘入口 + 附近美食流）
目标：3 秒知道"吃什么、去哪吃"。
```
Food decision app home "今天吃什么", 9:19.5, Chinese UI.
Top: location "国贸▾" + rounded search bar "搜菜品/餐厅/菜系".
Marquee: light orange #FFF3E8 bar, megaphone icon, scrolling "今日推荐：秋天第一顿火锅，3 家收藏破万…", close x.
Hero: big #FF4D2E rounded card, "今天吃什么？" huge white text + "点我帮你决定" + dice icon, subtle steam illustration.
Chips row (scrollable): 川菜/火锅/日料/轻食/烧烤/奶茶, selected filled #FF4D2E.
Feed: 2-col cards, each: appetizing food photo, bold shop name, rating "4.8★" in #FFC531, "¥85/人 · 500m", heart icon.
Bottom tab: 首页/发现/消息/我的. Background #FFF9F5, cards white 16px.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·首页`

### S4 随机决定页（定制：大转盘）
目标：选择困难症的解药，一键出结果。
```
Random food decider page, 9:19.5, Chinese UI, playful.
Center: big prize wheel divided into 8 segments (火锅/川菜/日料/烧烤/轻食/面馆/奶茶/随便), each with tiny food icon, #FF4D2E + #FFC531 alternating.
Center button "开吃！" bold white on #1A1D21 circle.
Result state variant: confetti, card "今日份答案：重庆火锅！" + shop photo + "就去这家" #FF4D2E button + "再转一次" text button.
Background #FFF9F5.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·随机转盘`

### S5 搜索页 [库06]
```
Search page, 9:19.5. Search bar "搜菜品/餐厅", #FF4D2E cursor.
"搜索历史" + trash: chips 火锅/螺蛳粉/减脂餐. "热搜榜": 10 rows, top3 #FF4D2E ranks, "秋天第一杯奶茶" with 热 badge.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·搜索`

### S6 关键词筛选页 [库07]
```
Filter page, 9:19.5. Groups: 菜系(川菜/粤菜/日料/西餐) / 人均(50以下/50-100/100-200) / 距离(1km内/3km内) / 口味(辣/清淡).
Selected pills filled #FF4D2E. Bottom: "重置" + #FF4D2E "确定(86家)".
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·关键词筛选`

### S7 餐厅详情页（定制）
```
Restaurant detail page, 9:19.5, Chinese UI.
Top: photo gallery (dishes + interior, swipe dots), back/share/heart overlaid.
Name "蜀大侠火锅(国贸店)" bold 22px, rating "4.8★" #FFC531 + "2.3万人吃过".
Info row: ¥85/人 · 川菜 · 距你500m · "排队12桌" red badge.
Signature dishes: horizontal scroll cards (毛肚/鸭血…).
Address card: mini map + "导航" button. Bottom sticky: white "收藏" + #FF4D2E "去吃！".
Background #FFF9F5, white 16px section cards.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·餐厅详情`

### S8 菜谱详情页（定制）
```
Recipe detail page, 9:19.5, Chinese UI.
Hero: big appetizing dish photo, title "番茄炒蛋（3 步版）", meta: 简单/15分钟/2人份.
Ingredient checklist with checkboxes: 番茄2个/鸡蛋3个/糖少许.
Steps: numbered 1-2-3 with small photos. Bottom #FF4D2E "加入本周菜单" + outline "收藏".
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·菜谱详情`

### S9 底部 Tab [库03]
```
Bottom tab: 首页/发现/中央凸起 #FF4D2E "吃什么" dice button/消息(badge 2)/我的. Selected #FF4D2E.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·底部Tab`

### S10 筛选底部弹窗 [库04]
```
Bottom sheet "筛选": drag handle, rows 菜系/人均/距离 with values + chevrons, bottom "重置" + #FF4D2E "确定".
```
封面：卡片 A｜`💥设计参考｜今天吃什么·底部弹窗`

### S11 分享底部弹窗（定制：帮我选）
```
Bottom sheet "分享给朋友帮我选": 3 candidate cards (dish photos + names) selectable with checkmarks,
buttons: 微信 / 朋友圈 / 复制链接, #FF4D2E "发起投票".
```
封面：卡片 A｜`💥设计参考｜今天吃什么·分享弹窗`

### S12 个人主页 [库10]
```
Profile "我的": gradient header #FF4D2E→#FF8A50, avatar + "干饭达人" + "Lv.5 吃货" badge.
Stats: 收藏 48 / 吃过 132 / 想去 26. Grid: 我的拼单/优惠券/菜谱/客服.
List: 积分签到(red dot)/吃货会员/设置.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·个人主页`

### S13 积分签到 [库11]（饭票体系）
```
Check-in "饭票": "我的饭票 860", 7-day calendar (5 gold checks, today pulsing #FF4D2E),
streak "再签2天得霸王餐抽奖券", big #FF4D2E "立即签到", coupon grid (满50减10/奶茶买一送一).
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·积分签到`

### S14 吃货会员订阅 [库15]
```
Paywall "吃货会员": crown, perks 每月霸王餐抽奖/专属折扣/免排队特权/生日蛋糕.
Pricing 月付¥19/季付¥49/年付¥129"最划算", big #FF4D2E "立即开通".
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·付费订阅`

### S15 更新弹窗 [库09]
```
Update dialog: hotpot illustration #FF4D2E tones, "发现新版本 v3.1.0", 3 bullets (转盘新增"不吃辣"模式…), #FF4D2E "立即更新" + "稍后再说".
```
封面：卡片 A｜`💥设计参考｜今天吃什么·更新弹窗`

### S16 美食集卡 [库13]
```
Event "集美食卡赢霸王餐": countdown, 4x2 slots for 8 cuisines (5 colored: hotpot/sushi icons…, 3 gray "?"),
progress 5/8, gradient #FF4D2E "抽卡(剩余2次)", tasks 下单+1/邀好友+2.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·集卡`

### S17 公告跑马灯 [库08]
```
Marquee variants: default light-orange "今日推荐…" + urgent #FF4D2E "暴雨天外卖延时公告".
```
封面：卡片 A｜`💥设计参考｜今天吃什么·跑马灯`

### S18 饭点小组件 [库14]
```
Widget sheet: weather pill "28° 晴", clock "11:42", countdown card "距午饭还有 00:18:20" with #FF4D2E progress ring,
mini calendar strip. Dark-mode variants below.
```
封面：卡片 A｜`💥设计赏析｜今天吃什么·时间控件`

## 黏土风系列标题清单（连载用）
`💥设计赏析｜今天吃什么·启动页` / `｜今天吃什么·首页` / `｜今天吃什么·随机转盘` / `｜今天吃什么·搜索` / `｜今天吃什么·关键词筛选` / `｜今天吃什么·餐厅详情` / `｜今天吃什么·菜谱详情` / `｜今天吃什么·底部Tab` / `｜今天吃什么·个人主页` / `｜今天吃什么·积分签到` / `｜今天吃什么·付费订阅` / `｜今天吃什么·集卡` —— 12 条连载，封面统一卡片 A。
