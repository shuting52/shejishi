# 项目全案示例：房屋出租 App《安住》

输入："做一个房屋出租 App" → 以下为模式 C 完整输出。

## 主题变量表
| 变量 | 值 |
|---|---|
| App 名 | 安住 |
| slogan | 好房子，不将就 |
| {主色} | #FF5A1F 活力橙 |
| {深色} | #101828 藏青 |
| {背景色} | #F6F7F9 |
| {圆角} | 16px 卡片 / 12px 按钮 / 全圆角胶囊 |
| 风格关键词 | 真实房源大图、价格大字突出、地图找房、年轻化 |

## IA 树
```
安住
├─ 启动页 → 首页
├─ Tab：首页 / 地图 / 消息 / 我的
│  ├─ 首页：搜索栏、跑马灯公告、快捷筛选 chips、房源卡片流
│  ├─ 地图找房：地图 + 价格气泡 + 底部房源卡片
│  ├─ 消息：房东/管家会话列表
│  └─ 我的：个人主页、积分签到、会员订阅、设置
├─ 房源详情页 / 搜索页 / 筛选页 / 预约看房页
├─ 弹窗：筛选底部弹窗、联系房东底部弹窗、更新弹窗
└─ 活动：租房节集卡
```

## 逐屏 Prompt 清单

### S1 启动页 [库01]
目标：品牌第一印象，橙色活力。
```
Mobile app splash screen "安住", 9:19.5. Background gradient #FF5A1F to #101828, subtle grain.
Center: white geometric logo (roof + keyhole), soft glow. Below: bold white "安住", slogan "好房子，不将就" in 60% white.
Bottom tiny text "v1.0.0". Premium, clean, no photo.
```
封面：卡片 A｜`💥设计赏析｜安住·启动页`

### S2 启动图标 [库02]
```
App icon, rounded square. Solid #FF5A1F background, subtle diagonal highlight.
Center: bold white glyph, house roof merged with keyhole, geometric, no text.
High contrast at small size. Show on light + dark backgrounds.
```
封面：卡片 A｜`💥设计赏析｜安住·启动图标`

### S3 首页（定制：搜索+跑马灯+筛选+房源流）
目标：3 秒内看到"能租什么房、多少钱"。
```
Mobile rental app home "安住", 9:19.5, Chinese UI.
Top: location "北京▾" + rounded search bar "搜索小区/地铁站/房源".
Marquee bar below: light orange #FFF3E8, megaphone icon, scrolling "平台公告：本周六海淀集中看房专场…", close x.
Filter chips row (scrollable): 全部/整租/合租/3000以下/两室/近地铁, selected filled #FF5A1F.
Feed: 2-column staggered cards, each: real apartment photo, bold price "¥4,200/月", tags "整租·两室", "距地铁500m", heart icon.
Bottom tab bar: 首页/地图/消息/我的, 首页 selected #FF5A1F.
Background #F6F7F9, cards white 16px radius.
```
封面：卡片 A｜`💥设计赏析｜安住·首页`

### S4 搜索页 [库06]
```
Search page "安住", 9:19.5. Search bar "搜索小区/地铁站", #FF5A1F cursor.
"搜索历史" + trash: chips "五道口/合租/两室". "热搜榜": 10 rows, top3 #FF5A1F ranks, "海淀整租" with 热 badge.
```
封面：卡片 A｜`💥设计赏析｜安住·搜索`

### S5 关键词筛选页 [库07]
```
Filter page, 9:19.5. Groups: 价格区间(2000以下/2000-4000/4000-6000/6000以上) / 户型(一室/两室/三室) / 租期(短租/长租).
Pills, selected filled #FF5A1F. Bottom bar: "重置" + #FF5A1F "确定(128套)".
```
封面：卡片 A｜`💥设计赏析｜安住·关键词筛选`

### S6 房源详情页（定制）
目标：价格+设施+位置+预约，一屏决策。
```
Rental listing detail page, 9:19.5, Chinese UI.
Top: photo gallery (3 apartment photos, swipe dots), back + share + heart icons overlaid.
Price block: huge bold "¥4,200/月" #FF5A1F, "整租·两室一厅·68㎡" gray.
Facility icon grid 4x2: 床/空调/洗衣机/冰箱/WiFi/电梯/暖气/阳台.
Location card: mini map + "距地铁13号线五道口站 500m".
Landlord card: avatar "房东王先生", "已验证" badge, button "联系房东".
Bottom sticky bar: white "收藏" + #FF5A1F "预约看房".
Background #F6F7F9, sections white 16px cards.
```
封面：卡片 A｜`💥设计赏析｜安住·房源详情`

### S7 地图找房页（定制）
```
Map-based rental search, 9:19.5. Full-screen city map (Beijing), price bubbles "¥3.2k/¥4.2k/¥5.8k" on compounds, selected bubble #FF5A1F enlarged.
Top: search bar + filter chips floating. Bottom: draggable card showing nearest listing photo + price + distance.
```
封面：卡片 A｜`💥设计赏析｜安住·地图找房`

### S8 预约看房页（定制·时间选择）
目标：选日期+时间段，一键预约。
```
Viewing appointment page, 9:19.5, Chinese UI.
Listing mini-card top (photo + "¥4,200/月·五道口两室").
Date strip: 7 days horizontal, selectable, today ringed #FF5A1F.
Time slots grid 3 cols: 09:00/10:30/14:00/15:30/17:00, selected filled #FF5A1F, booked grayed "约满".
Note input "给房东留言（选填）". Bottom #FF5A1F button "确认预约".
Success state variant: checkmark + "预约成功，周六 10:30 见".
```
封面：卡片 A｜`💥设计赏析｜安住·预约看房`

### S9 底部 Tab [库03]
```
Bottom tab: 首页/地图/发布(中央凸起 #FF5A1F +号)/消息(badge 3)/我的. Selected #FF5A1F, 3 states: default / badge / pressed.
```
封面：卡片 A｜`💥设计赏析｜安住·底部Tab`

### S10 筛选底部弹窗 [库04]
```
Bottom sheet: drag handle, 20px top radius, title "筛选", rows 价格区间/户型/朝向 each with value + chevron, bottom "重置" + #FF5A1F "确定".
```
封面：卡片 A｜`💥设计参考｜安住·底部弹窗`

### S11 联系房东底部弹窗（定制）
```
Bottom sheet "联系房东王先生": avatar + "已验证" + response rate "通常2小时内回复".
Buttons: #FF5A1F "打电话" / outline "发消息" / text "举报".
```
封面：卡片 A｜`💥设计参考｜安住·联系房东`

### S12 个人主页 [库10]
```
Profile "我的": gradient header #FF5A1F→#FF8A50, avatar + "租房达人" + gold VIP.
Stats: 收藏 12 / 预约 3 / 优惠券 5. Grid: 我的预约/合同/账单/客服.
List: 积分签到(red dot)/会员订阅/设置.
```
封面：卡片 A｜`💥设计赏析｜安住·个人主页`

### S13 积分签到 [库11]
```
Check-in: "我的积分 1,280", 7-day calendar (5 gold checks, today pulsing #FF5A1F), streak banner "再签2天得50积分", big #FF5A1F "立即签到", coupon grid (租房券50元/保洁券).
```
封面：卡片 A｜`💥设计赏析｜安住·积分签到`

### S14 会员订阅 [库15]
```
Paywall "开通安住会员": crown, 4 perks (免中介费/优先看房/专属客服/每月租房券).
Pricing 月付¥29/季付¥69/年付¥199"最划算", big #FF5A1F "立即开通".
```
封面：卡片 A｜`💥设计赏析｜安住·付费订阅`

### S15 更新弹窗 [库09]
```
Update dialog: rocket illustration #FF5A1F tones, "发现新版本 v2.3.0", 3 changelog bullets, #FF5A1F "立即更新" + "稍后再说".
```
封面：卡片 A｜`💥设计参考｜安住·更新弹窗`

### S16 租房节集卡 [库13]
```
Event "租房节·集卡赢免租": countdown, 4x2 slots (5 colored: sofa/key/plant…, 3 gray "?"), progress 5/8, gradient #FF5A1F "抽卡(剩余3次)", tasks 浏览房源/邀好友.
```
封面：卡片 A｜`💥设计赏析｜安住·集卡`

## 黏土风系列标题清单（连载用）
`💥设计赏析｜安住·启动页` / `｜安住·启动图标` / `｜安住·首页` / `｜安住·搜索` / `｜安住·关键词筛选` / `｜安住·房源详情` / `｜安住·地图找房` / `｜安住·预约看房` / `｜安住·底部Tab` / `｜安住·个人主页` / `｜安住·积分签到` / `｜安住·付费订阅` —— 12 条连载，封面统一卡片 A，形成账号矩阵。
