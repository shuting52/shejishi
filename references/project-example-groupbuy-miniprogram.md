# 项目全案示例：社区团购小程序《邻里团》

输入："做一个社区团购小程序" → 模式 C 完整输出（按 miniprogram-notes.md 做了小程序适配）。

## 主题变量表
| 变量 | 值 |
|---|---|
| 小程序名 | 邻里团 |
| slogan | 邻里一起买，又鲜又便宜 |
| {主色} | #FF4D2E 番茄红（促销感） |
| {深色} | #1A1D21 炭黑 |
| {背景色} | #FFF9F5 暖米白 |
| 点缀色 | #22B573 生鲜绿 / #FFC531 芥末黄 |
| {圆角} | 16px 卡片 / 12px 按钮 / 全圆角胶囊 |
| 风格关键词 | 生鲜、拼团、倒计时、邻里信任感 |
| 吉祥物 | 白团子快递员（抱着菜篮子） |

## IA 树
```
邻里团（小程序）
├─ 分享/搜索进入 → 首页（自提点模式，无启动页）
├─ Tab：首页 / 秒杀 / 购物车 / 我的
│  ├─ 首页：定位+自提点▾ / 搜索 / 秒杀倒计时条 / 分类 / 今日团购流
│  ├─ 秒杀：整点场倒计时 + 秒杀商品流（库24）
│  ├─ 购物车：商品行 + 凑单提示
│  └─ 我的：微信头像昵称 / 待提货 / 优惠券 / 团长中心 / 客服
├─ 商品详情页（拼团价/单买价/开团/参团）
├─ 结算页（自提点/自提时间/微信支付）
├─ 订单列表/详情（提货码）
├─ 弹窗：拼团进度异形弹窗 / 规格底部弹窗 / 分享开团底部弹窗 / 自提点选择底部弹窗
└─ 活动：签到领菜金（库11）、分享开团
```

## 逐屏 Prompt 清单

### S1 小程序分享卡（替代库01/02）
```
WeChat mini-program share card "邻里团", 5:4 landscape, Chinese.
Background warm cream #FFF9F5 with fresh vegetable pattern border.
Left: bold #1A1D21 "今日团购 5 折起" + red #FF4D2E "邻里一起买更便宜".
Right: white clay dumpling courier mascot hugging vegetable basket.
Bottom-right: mini-program QR placeholder in white rounded square.
Fresh, trustworthy, readable at chat thumbnail size.
```
封面：卡片 A｜`💥设计赏析｜邻里团·分享卡`

### S2 首页（定制：自提点 + 倒计时）
目标：3 秒知道"今天团什么、去哪提"。
```
Group-buy mini-program home "邻里团", 9:19.5, Chinese UI.
Custom nav: left "📍幸福小区·3号自提点▾", right clear for capsule.
Search "搜生鲜/日用" + scan.
Flash strip: #FF4D2E bar, "⏰ 今日秒杀 20:00 开抢" + countdown 02:14:33 (semantic: 时/分/秒 labels).
Category chips: 蔬菜/水果/肉蛋/粮油/日用.
Feed: 2-col cards: product photo, name "山东大樱桃 500g", 拼团价 "¥19.9" red bold + 单买价 "¥29.9" strikethrough, progress "已拼 82%" bar, #FF4D2E "去拼团".
Bottom tab: 首页/秒杀/购物车(badge 2)/我的. Safe-area padding.
```
封面：卡片 A｜`💥设计赏析｜邻里团·首页`

### S3 秒杀频道 [库24]
目标：倒计时制造紧迫感，库存诚实。
```
Flash sale page: header #1A1D21, "整点秒杀" + 3 session tabs 10:00(已开抢)/14:00(即将开始)/20:00(预告).
Countdown big mono digits with 时/分/秒 labels (semantic, not bare numbers).
Product rows: photo, name, 秒杀价 red + 原价 strikethrough, stock bar "仅剩 12%", button states:
 进行中 #FF4D2E "马上抢" / 即将开始 disabled gray "即将开始" + honest "开抢提醒我（订阅消息）" / 已抢光 gray "已抢光" (no fake CTA).
```
封面：卡片 A｜`💥设计赏析｜邻里团·秒杀`

### S4 商品详情页（定制：拼团双价）
目标：拼团价 vs 单买价，一眼选拼团。
```
Product detail, 9:19.5, Chinese UI.
Gallery: product photos swipe dots. Title "山东大樱桃 500g · 现摘现发".
Price card: left "拼团价 ¥19.9" red 28px + "单买价 ¥29.9" strikethrough + badge "拼团省¥10".
Group rows: "2 人团 · 还差 1 人" avatars + countdown 11:23 + #FF4D2E "参团";
"开新团" outline button. Rules link "拼团玩法".
Specs: 规格/产地/保质期 rows. Reviews strip. Sticky bottom: "单买 ¥29.9" outline + #FF4D2E "开团 ¥19.9".
```
封面：卡片 A｜`💥设计赏析｜邻里团·商品详情`

### S5 拼团进度异形弹窗 [库28]
目标：把"差几人"写清楚，分享 CTA 突出。
```
Irregular popup "拼团进度": rounded ticket shape, header "还差 1 人成团！" 24px bold (not just color: big number).
Avatars row: 2 filled + 1 dashed "?" slot. Countdown "剩余 11:23:45" with 时/分/秒 labels.
Honest copy: "到期未成团自动退款". Big #FF4D2E "邀请好友拼团" + text "分享到微信".
Close X. States: success → confetti + green "拼团成功！" + "去下单".
```
封面：卡片 A｜`💥设计赏析｜邻里团·拼团弹窗`

### S6 结算页 [库29]
```
Checkout: 自提点 card "幸福小区3号自提点 · 王阿姨 138****1234" + "切换" + 自提时间 segmented 今天16:00后/明天上午.
Remark input "备注…". Payment: 微信支付 selected.
Summary rows + 菜金抵扣 "-¥5". Sticky: "实付 ¥24.9" + #FF4D2E "微信支付".
Empty coupon → honest "暂无可用优惠券".
```
封面：卡片 A｜`💥设计赏析｜邻里团·结算页`

### S7 订单列表/详情 [库31]
```
Orders tabs: 待提货/已完成/退款.
Card 待提货： "山东大樱桃x2" + orange "待提货" + 提货码 "提货码 8823" bold + #FF4D2E "出示提货码".
Detail: timeline 下单→备货中→待提货 (current highlighted, not color-only: check icons),
pickup info card: 自提点地址 + 导航 button + 联系团长 button.
Empty: mascot + "还没有订单" + "去逛逛" CTA.
```
封面：卡片 A｜`💥设计赏析｜邻里团·订单`

### S8 购物车（定制：凑单）
```
Cart: rows with steppers, "凑单" strip: "再买 ¥12 可用满50减10券" + progress bar + #FF4D2E "去凑单".
Invalid items group: gray "已下架" + "清空失效商品" (honest, not hidden).
Bottom: "合计 ¥38" + big #FF4D2E "去结算(3)". Empty: mascot + "购物车空空" + "去首页逛逛" CTA.
```
封面：卡片 A｜`💥设计参考｜邻里团·购物车`

### S9 我的 [库10 + 团长入口]
```
Profile: cream header, WeChat avatar + nickname / "微信一键登录" green button.
Stats: 待提货 2 / 优惠券 5 / 菜金 ¥12.5.
Grid: 我的订单/拼团中/优惠券/收货地址.
团长横幅 (if 团长）: green card "团长中心 →" + "今日待提货 18 单".
List: 订阅消息管理（成团通知/到货通知 开关）/ 联系客服 / 设置.
```
封面：卡片 A｜`💥设计赏析｜邻里团·我的`

### S10 团长中心（定制）
```
Captain dashboard: header "王阿姨 · 幸福小区3号自提点", stats cards 今日订单 24 / 待提货 18 / 佣金 ¥86.5.
Tabs: 待提货（提货码核销按钮）/ 已完成. Big #22B573 "扫码核销" button.
Announcement input "发布到货通知" → 订阅消息群发（需用户授权说明）.
```
封面：卡片 A｜`💥设计赏析｜邻里团·团长中心`

### S11 签到领菜金 [库11]
```
Check-in "菜金": "我的菜金 ¥12.5", 7-day strip (5 green checks, today pulsing #FF4D2E),
"连续签到7天得 ¥5 菜金", big #FF4D2E "立即签到", tasks 下单+2/邀好友+5.
```
封面：卡片 A｜`💥设计赏析｜邻里团·签到`

### S12 自提点选择底部弹窗 [库04]
```
Bottom sheet "选择自提点": search "搜小区/自提点", rows (name + distance + 团长名 + "营业中" green badge),
selected row #FF4D2E check + bold (not color-only). Bottom #FF4D2E "确定".
```
封面：卡片 A｜`💥设计参考｜邻里团·自提点`

### S13 分享开团底部弹窗 [库04]
```
Bottom sheet "分享开团": product mini card + "2人团 ¥19.9/人",
buttons 分享给微信好友 (green) / 分享到朋友圈， #FF4D2E "发起拼团".
Preview of share card with mini-program code.
```
封面：卡片 A｜`💥设计赏析｜邻里团·分享开团`

## 小程序差异点（本案）
- 无启动页/图标/更新弹窗 → S1 分享卡、骨架屏
- 自提点是核心地理概念（替代门店）：选择器 + 切换 + 团长
- 订阅消息：成团通知/到货通知/秒杀提醒（全部需用户授权，开关放在我的页）
- 微信支付唯一；分享链路全部走微信好友/朋友圈

## 黏土风系列标题清单（连载用）
`💥设计赏析｜邻里团·分享卡` / `｜邻里团·首页` / `｜邻里团·秒杀` / `｜邻里团·商品详情` / `｜邻里团·拼团弹窗` / `｜邻里团·订单` / `｜邻里团·团长中心` / `｜邻里团·签到` —— 8 条连载，封面统一卡片 A。
