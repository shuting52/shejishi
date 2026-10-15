# 项目全案示例：扫码点餐小程序《快点餐》

输入："做一个扫码点餐小程序" → 模式 C 完整输出（按 miniprogram-notes.md 做了小程序适配）。

## 主题变量表
| 变量 | 值 |
|---|---|
| 小程序名 | 快点餐 |
| slogan | 扫码就点，上菜更快 |
| {主色} | #FF4D2E 番茄红（食欲感） |
| {深色} | #1A1D21 炭黑 |
| {背景色} | #FFF9F5 暖米白 |
| 点缀色 | #FFC531 芥末黄 |
| {圆角} | 16px 卡片 / 12px 按钮 / 全圆角胶囊 |
| 风格关键词 | 食欲感、快、堂食扫码、加购爽快 |
| 吉祥物 | 白团子厨师（端托盘） |

## IA 树
```
快点餐（小程序）
├─ 扫码进入 → 首页（门店模式，无启动页）
├─ Tab：点餐 / 订单 / 我的
│  ├─ 点餐：自定义导航（门店名▾，避让胶囊）/ 搜索 / 分类TAB / 菜品流 / 底部购物车栏
│  ├─ 订单：进行中 / 待评价 / 已完成 / 退款（库31 四态）
│  └─ 我的：微信头像昵称 / 我的订单 / 优惠券 / 订阅消息管理 / 客服
├─ 菜品详情页（大图 + 规格选择）
├─ 结算页（取餐方式/备注/微信支付）
├─ 订单详情页（取餐码）
├─ 弹窗：规格底部弹窗 / 购物车底部弹窗 / 取餐码异形弹窗 / 排号异形弹窗 / 分享拼单底部弹窗
└─ 跑马灯：门店公告（今日例汤/高峰期提示）
```

## 逐屏 Prompt 清单

### S1 小程序分享卡（替代库01/02）
目标：微信聊天里一眼想点。
```
WeChat mini-program share card "快点餐", 5:4 landscape, Chinese.
Background #FF4D2E with subtle steam pattern.
Left: bold white "扫码点餐，不用排队" + small "快点餐 · 国贸店可用".
Right: cute white clay dumpling chef mascot holding tray.
Bottom-right: mini-program QR code placeholder in white rounded square.
Appetizing, high contrast, readable at chat thumbnail size.
```
封面：卡片 A｜`💥设计赏析｜快点餐·分享卡`

### S2 点餐首页（定制，避让胶囊）
目标：3 秒找到想吃的，加购路径最短。
```
Food ordering mini-program home "快点餐", 9:19.5, Chinese UI.
Custom nav: left "蜀大侠火锅(国贸店)▾", right side kept clear for WeChat capsule button.
Search bar "搜菜品，如毛肚" + scan icon.
Category tabs (scrollable): 招牌/火锅荤菜/素菜/小吃/饮品, selected #FF4D2E underline + bold.
Dish feed: cards with appetizing photo, name "鲜毛肚", "¥32/份", sales "月售1200+", stepper (+/-) #FF4D2E.
Sticky bottom cart bar: white, "购物车 🛒3" + "¥96" + big #FF4D2E "去结算".
Background #FFF9F5. Safe-area padding at bottom.
```
封面：卡片 A｜`💥设计赏析｜快点餐·点餐首页`

### S3 规格底部弹窗 [库04]
```
Bottom sheet "鲜毛肚": dish photo top, spec groups 份量(小份/大份)/辣度(微辣/中辣)/加料(香菜+2/蒜泥+2),
stepper, bottom bar "¥36" + #FF4D2E "加入购物车". Drag handle, rounded 20px top.
```
封面：卡片 A｜`💥设计参考｜快点餐·规格弹窗`

### S4 购物车底部弹窗 [库04]
```
Bottom sheet "已选 3 件": rows (鲜毛肚x2 ¥64 / 冰粉x1 ¥12) with steppers,
"清空" text button, subtotal "¥96", big #FF4D2E "去结算". Empty state: mascot + "购物车空空如也" + "去加购" CTA.
```
封面：卡片 A｜`💥设计参考｜快点餐·购物车`

### S5 结算页 [库29]
目标：信息一次填对，支付一步到位。
```
Checkout page, 9:19.5, Chinese UI.
Sections (white 16px cards): 取餐方式 segmented 堂食(桌号A12)/自提；备注 input "忌口、少辣…";
Payment: 微信支付 selected (green check), no other options.
Order summary rows + coupon "-¥10 新人券". Sticky bottom: "实付 ¥86" + big #FF4D2E "微信支付 ¥86".
States: empty coupon → mascot + "暂无可用优惠券" (no CTA, honest).
```
封面：卡片 A｜`💥设计赏析｜快点餐·结算页`

### S6 订单列表 [库31 四态]
```
Orders page, 9:19.5. Tabs: 进行中/待评价/已完成/退款.
Card 进行中： "蜀大侠火锅" + orange "备餐中" + countdown "预计12分钟" + #FF4D2E "查看取餐码".
Card 待评价： gray "已完成" + outline "去评价".
Card 退款中： red badge "退款审核中" + disabled-looking but honest "预计1-3天到账".
Empty: mascot + "还没有订单" + "去点餐" CTA.
```
封面：卡片 A｜`💥设计赏析｜快点餐·订单列表`

### S7 取餐码异形弹窗 [库28]
目标：举着手机给店员看，一眼可读。
```
Irregular popup "取餐码": ticket shape with perforated edge, #FF4D2E header "备餐中".
Giant number "A128" 64px bold, barcode below, "蜀大侠火锅 · 桌号A12".
Countdown ring "预计 08:32". Screenshot-proof: high contrast, no tiny text.
Close X top-right. States: ready → header turns green "可取餐" + vibration hint.
```
封面：卡片 A｜`💥设计赏析｜快点餐·取餐码`

### S8 排号异形弹窗 [库28]
```
Irregular popup "排号": cloud shape, "前面还有 3 桌" huge, "预计等待 25 分钟",
progress "已等 10 分钟", #FF4D2E "到号叫我" (subscribe message auth), text "取消排号".
```
封面：卡片 A｜`💥设计参考｜快点餐·排号`

### S9 评价页（定制）
```
Rating page: 5 big stars (tap to light, not color-only: number "4.8分" shown),
tag chips 好吃/上菜快/分量足/服务好 (multi-select, selected filled #FF4D2E + check),
photo upload slots, textarea "说说你的感受…", big #FF4D2E "提交评价".
```
封面：卡片 A｜`💥设计赏析｜快点餐·评价`

### S10 我的 [库10 + 微信登录]
```
Profile "我的": cream header, WeChat avatar + nickname "微信一键获取" button (green) if not authorized.
Stats: 订单 36 / 优惠券 3 / 积分 860.
Grid: 我的订单/优惠券/排号记录/发票.
List: 订阅消息管理（取餐通知 开/关）/ 联系客服 / 关于.
```
封面：卡片 A｜`💥设计赏析｜快点餐·我的`

### S11 优惠券 [库30 空态]
```
Coupons: tabs 未使用/已使用/已过期. Card: ¥10满50可用， dashed divider, "去使用".
Empty 未使用： mascot + "暂无可用优惠券" + honest copy "新人券已发完，下次早点来" (no fake CTA).
```
封面：卡片 A｜`💥设计参考｜快点餐·优惠券`

### S12 门店公告跑马灯 [库08]
```
Marquee: light orange bar, 📢 "今日例汤：番茄牛腩 | 高峰期 12:00-13:00 建议提前点", close x.
Urgent variant #FF4D2E: "后厨设备维护，今日 15:00 后暂停接单".
```
封面：卡片 A｜`💥设计参考｜快点餐·跑马灯`

### S13 分享拼单底部弹窗 [库04]
```
Bottom sheet "喊朋友一起拼": order summary card + "AA拼单" toggle,
buttons: 分享给微信好友 (green) / 生成拼单码, #FF4D2E "发起拼单".
Mini-program code embedded in share card preview.
```
封面：卡片 A｜`💥设计赏析｜快点餐·分享拼单`

## 小程序差异点（本案）
- 无启动页/图标/更新弹窗 → S1 分享卡、骨架屏、版本提示条
- 自定义导航栏避让微信胶囊；底部安全区
- 微信一键登录；订阅消息（取餐/排号叫号）；微信支付唯一选项

## 黏土风系列标题清单（连载用）
`💥设计赏析｜快点餐·分享卡` / `｜快点餐·点餐首页` / `｜快点餐·结算页` / `｜快点餐·订单列表` / `｜快点餐·取餐码` / `｜快点餐·评价` / `｜快点餐·我的` —— 7 条连载，封面统一卡片 A。
