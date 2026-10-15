# 组件设计 Prompt 库（15 个通用组件）

每个组件一张卡：定义 → 设计要点 → UI 生成提示词（直接投喂 Figma AI / 即梦 / v0 / Galileo 等 AI 界面工具）→ 黏土风封面推荐。

主题变量（项目全案模式下统一填入，单组件模式用默认值）：
`{主色}` 默认 #FF5A1F ｜ `{深色}` 默认 #101828 ｜ `{背景色}` 默认 #F6F7F9 ｜ `{圆角}` 默认 16px ｜ `{字体}` 默认粗黑体标题+常规正文

---

## 01 启动页 Splash
**定义**：App 冷启动时的品牌展示页，1~2 秒。
**设计要点**：品牌 logo 居中或居上；slogan 一句话；背景用品牌主色渐变或纯色；可加 subtle 动效示意（logo 浮现）；底部小字版本号/备案。
**UI 生成提示词**：
```
Mobile app splash screen, 9:19.5 vertical, Chinese UI.
Background: gradient from {主色} to {深色}, subtle grain texture.
Center: minimalist app logo mark (house/key abstract icon), white, with soft glow.
Below logo: bold white Chinese app name, letter-spaced; one-line slogan in 60% white.
Bottom: tiny light text "v1.0.0".
Style: premium, clean, no photo, generous negative space.
```
**黏土风封面**：卡片 A；标题 `💥设计赏析｜启动页`

## 02 启动图标 App Icon
**定义**：桌面图标，圆角矩形，强识别。
**设计要点**：单一图形符号（项目核心意象）；主色底或深色底；避免细小文字；iOS/Android 圆角适配。
**UI 生成提示词**：
```
App icon design, rounded square, flat vector style.
Background: solid {主色} with subtle diagonal highlight.
Center: single bold white glyph combining house roof + keyhole, geometric, no text, no fine details.
High contrast, recognizable at small size, no shadows overload.
Present on light and dark mock backgrounds.
```
**黏土风封面**：卡片 A；标题 `💥设计赏析｜启动图标`

## 03 底部 Tab Bar [实测：用户 7 张截图之 3 张底部TAB封面]
**定义**：App 主导航，3~5 个 tab。
**设计要点（7 套图标风格全收录）**：
- A 荧光描边：未选中细线稿 → 选中黑底 + 荧光绿描边 + 内部小图形
- B 局部填色：dictionary/translation/class/discovery/mine，英文小字；选中局部填粉红
- C 吉祥物：首页/地图/搭子/我的；未选中黑剪影 → 选中绿紫渐变吉祥物
- D 圆底座：圆形底座 + 线稿；选中底座内图标填绿
- E 中英双语：首页/发现/会员/我的 + HOME PAGE/FIND/MEMBER/MY；选中图标绿填充
- F 全英文：HOME/FIND/GAME/MINE；选中绿描边
- G 点缀色：首页/找图/圈子/我的；选中图标加粉色点缀
- 选中态三手法：填充色块 / 描边变色 / 局部填色；中英双语标签是她的常用格式
**UI 生成提示词**：
```
Mobile app bottom tab bar icon set showcase, 9:19.5, Chinese UI.
White rounded card on black background, two rows: top row 4 unselected icons (thin black line style): home / map pin / chat / profile;
bottom row the same 4 icons in SELECTED state: solid black fill with neon green (#B6FF5C) outline glow + tiny inner graphic.
Below: second card with 5 tabs: dictionary / translation / class / discovery / mine, English small gray labels under icons; selected state = partial pink fill on icon.
Style: cute, bold, high contrast between selected/unselected.
Also show a mascot variant: 4 tabs （首页/地图/搭子/我的） where unselected = black silhouette mascot, selected = green-purple gradient mascot.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"底部TAB" + 白卡图标矩阵（未选中/选中两行对比）；标题 `💥设计赏析｜底部TAB`

## 04 底部弹窗 Bottom Sheet [实测：用户 8 张截图之 5 张底部弹窗封面]
**定义**：从底部升起的操作面板，半屏或全屏。
**通用骨架**：顶部圆角 + 小把手/装饰 → 大标题 + 吉祥物 → 内容区（权益卡/金额宫格/品牌宫格/功能列表）→ 底部大 CTA → 右上 X 关闭。
**设计要点（8 版式全收录）**：
- A 选课："帮你选课提升 资深教师|限时免费送"；权益卡（专属学习规划/1v1学情分析/免费精讲课程/400元优惠券）；"全部收下！"
- B 花呗10周年："花呗10周年 新了一点"；"领取你的花呗10周年礼包"；品牌宫格（生日快乐气泡+321）；品牌名（闲鱼/NBA/滴滴/饿了么/飞猪）
- C 家庭中心："家庭中心3大权益 让家庭管理更便捷"；01/02/03（免绑户号代缴费/共享记录全员查/在线提醒少逾期）；"立即创建家庭中心"
- D 充值："别错过你们的缘分"；金额宫格（10/65/300/1050/3150/5550，"首充"角标）；"19.00"+"充值"
- E 资产："我的资产"；金币6/钻石0；"今天"流水（解锁累计售出任务+3/出售满分蛋粽+3)；"—没有更多了—"
- F 温馨守护："温馨守护" + 爱心；"功能一 签约自动续费提醒 / 功能二 大额消费提醒"；"稍后了解/邀请亲友"
- G 行程结束："V7会员 行程已顺利结束 里程值+2.8"；司机卡（屠师傅 快车 合计14.70元）；"开发票/联系客服/感谢红包"；"免费感谢司机师傅 百万免费感谢红包"；"谢谢TA"
- H 拍立得："2022 06/20"拍立得风；猫照片 + "MEOW~"；"今日富豪喵：四月"+"我也想上榜>>"；"开心收下"
- 通用铁律：标题永远配吉祥物/插画；CTA 是品牌色大按钮；金额类用宫格 + "首充"角标；右上 X 必备
**UI 生成提示词**：
```
Mobile bottom sheet popup, 9:19.5, Chinese UI, over dimmed app content (40% black overlay).
Show 2 variants side by side:
Variant 1 (course): white sheet, top rounded 24px with drag handle. Big title "帮你选课提升" + orange "资深教师 | 限时免费送". 4 benefit cards: 专属学习规划/1v1学情分析/免费精讲课程/400元优惠券， each with cute illustration. Orange CTA "全部收下！". Close X top-right.
Variant 2 (family): white sheet, title "家庭中心3大权益" + subtitle "让家庭管理更便捷 让每一份爱被看见". 3 numbered columns 01/02/03: 免绑户号代缴费/共享记录全员查/在线提醒少逾期， each with icon + tag （家人代缴/家庭月报/出账提醒）. Orange CTA "立即创建家庭中心".
Cute mascot peeking from top edge of sheet.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"底部弹窗" + 弹窗拼贴；标题 `💥设计赏析｜底部弹窗`

## 05 主题 UI 配色 Theme
**定义**：整套 App 的色彩/字体/圆角规范展示图。
**设计要点**：主色+深色+背景+成功/警示+文字三级灰；色卡带色值；字体层级示例；圆角/阴影示例。
**UI 生成提示词**：
```
UI design system style tile, 16:9 landscape poster, Chinese labels.
Left: 5 large color swatches with hex codes: primary {主色}, dark {深色}, background {背景色}, success #12B76A, alert #F04438.
Middle: typography scale samples: 28px bold headline / 16px body / 12px caption, Chinese text.
Right: corner radius samples ({圆角} card, 12px button, full pill), button styles (primary filled, outline, text).
Dark section at bottom showing dark-mode mapping.
Clean spec-sheet layout, grid aligned.
```
**黏土风封面**：卡片 D；标题 `💥设计参考｜主题配色`

## 06 搜索 Search
**定义**：搜索页 = 搜索框 + 历史 + 热搜。
**设计要点**：搜索框圆角胶囊常驻顶部；历史词可删除/一键清空；热搜带排名色块；空结果状态。
**UI 生成提示词**：
```
Mobile app search page, 9:19.5, Chinese UI.
Top: rounded search bar with magnifier icon, placeholder "搜索房源/小区/地铁站", {主色} cursor.
Section 1 "搜索历史" with trash icon: 6 pill-shaped history chips, one with long-press delete "x".
Section 2 "热搜榜": 10 rows, rank 1-3 in {主色} numbers, rest gray, each with topic text + "热" flame badge on top3.
Empty state variant: illustration + "试试搜索你感兴趣的内容".
Background {背景色}, cards white {圆角}.
```
**黏土风封面**：卡片 A；标题 `💥设计赏析｜搜索页`

## 07 关键词筛选 Filter Chips [实测：用户 8 张截图之 4 张关键词筛选封面]
**定义**：多选标签组（兴趣/偏好/筛选），不止横滑 chips。
**设计要点（7 版式全收录）**：
- A 词云胶囊：吉祥物 + 引用式标题，彩色胶囊多角度散布（大小/颜色/旋转各异），黑"下一步"
- B 异形标签：灰色三角/圆/方异形标签（少淑/甜酷/辣妹/名媛…），右上"已选0个"计数，未选 CTA 置灰"选好了"
- C 圆形+计数：顶部 Tab 分类 + 圆形标签，选中变青色圆；"- 已选择3，还可以选择7个 -"；已选胶囊可删（×）；黑"下一步"
- D 便利贴：彩色便利贴卡片，标题 + 一句描述，错落排布
- E 星空关键词："点亮✦ 感兴趣的内容"，关键词星空散布（部分带图），底部"关注3个兴趣标签进入"黑胶囊 + "跳过直接进入"
- F 分组多选：三组白卡（心情/口味/量），卡内胶囊多选，选中黑底；底部"随机一下/今日特调"双按钮
- G 气泡球：大气泡球为选中态（含图），小灰球未选；"下一步（已选2个）"蓝渐变按钮
- 通用：选中态必须一眼可辨（变色/变底/加框三选一）；计数文案（已选N个/还可选N个）；未选 CTA 置灰
**UI 生成提示词**：
```
Mobile interest-tag selection page, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (bubble): title "选择你感兴趣的音乐标签", subtitle "你的选择将获取更精准的推荐哦～". Floating bubbles of different sizes: one large blue bubble "流派" with cassette illustration (selected), small gray bubbles "嘻哈/R&B/流行/电子/民谣/国风/独立/摇滚/古典/爵士/语种". Bottom blue gradient button "下一步（已选2个）".
Variant 2 (grouped cards): light blue background, title "今天想喝点什么？". 3 white cards: "此刻的你心情如何呢？" with emoji pills (开心/无感/满足/难过/我的心情我定义), "想来一杯什么口味的酒呢" with pills (酸酸的/甜甜的/劲辣的/偏苦的), "不醉不归 or 小酌一杯？" with pills. Selected pills black background white text. Bottom: two buttons "随机一下" outline + "今日特调" black.
Playful, colorful, clear selected states.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"关键词筛选" + 下方双手机截图拼贴；标题 `💥设计赏析｜关键词筛选`

## 08 公告跑马灯 Marquee
**定义**：顶部滚动公告条。
**设计要点**：喇叭图标+单行滚动文字；可关闭；重要公告用主色底。
**UI 生成提示词**：
```
Mobile app home screen top area, 9:19.5, Chinese UI.
Below search bar: announcement marquee bar, light orange background (#FFF3E8), megaphone icon in {主色}, single-line scrolling text "平台公告：本周六海淀区集中看房专场…", close "x" on right.
Show 2 variants stacked: default marquee + urgent version with {主色} background white text.
Rest of screen: blurred home content behind.
```
**黏土风封面**：卡片 A；标题 `💥设计参考｜公告跑马灯`

## 09 更新弹窗 Update Dialog
**定义**：版本更新提示弹窗。
**设计要点**：居中卡片；新功能 3 条 bullet；"立即更新"主按钮 + "稍后再说"；强制更新时无关闭。
**UI 生成提示词**：
```
Mobile app update dialog, 9:19.5, Chinese UI, dimmed background.
Centered white card {圆角} 20px, top illustration (rocket, {主色} tones).
Title "发现新版本 v2.3.0", 3 bullet changelog lines with check icons.
Two buttons: primary {主色} "立即更新", text button "稍后再说".
Second variant: force-update with single button and no close icon.
```
**黏土风封面**：卡片 A；标题 `💥设计参考｜更新弹窗`

## 10 个人主页 Profile [实测：用户 7 张截图之 3 张个人主页封面]
**定义**："我的"页 = 用户信息 + 功能入口。
**通用骨架（6 屏验证）**：顶部区（头像+昵称+ID+设置/编辑）→ 数据行（3-4 个数字）→ 会员/资产横幅 → 功能宫格 → 列表 → （动态流）。
**设计要点（6 版式全收录）**：
- A 社交版：数据行（好友/关注/粉丝/访客）；会员横幅"开通解锁13大会员特权"+"立即开通"；宫格（我的钱包/幸运签到/认证/收益/任务/道具商城/背包/邀请赚钱）；开关行（语音通话/视频通话/匹配接听）；设置行（聊天设置/女神权益/贵族/我的成就）
- B 任务版："资料完善度50%"；双卡（我的钱包/文撩商城）；任务中心（7天签到横滑）；常用功能 12 宫格（会员中心/我的动态/邀请好友/亲密鹦群/认证中心/我的相册/我的等级/美颜设置/青少年模式/账号安全/联系客服/社区规范/系统设置）
- C 直播版：绿渐变顶；"完善资料领好礼"；"我的资产"（钻石/金币）；魅力值/财富值双卡；常用功能（礼物墙/关系/师徒/森友会）；个人功能（动态/战绩/成就/等级/背包/任务/商城/称号）
- D 宠物版：青绿顶 + 吉祥物 + HELLO~气泡；数据行（胖豆/关注/粉丝/获赞）；"添加我的爱宠"；功能行（每日签到/胖豆商城/邀请好友）；动态/赞过/活动 Tab + 动态流
- E 未登录版：黄绿渐变顶"登录/注册"；会员横幅"开通会员，解锁10+尊享特权"+皇冠+4特权图标；双卡（我的消息/我的收藏）；通知横幅"开启通知权限"；列表（五星好评/帮助中心/意见反馈）
- F 健康版：绿渐变顶"点击登录"；会员横幅"轻食Go会员中心 终身会员限时98元"；功能行（我的目标/+微信群/+QQ群/赏个好评）；内容卡（助教一对一/断食小知识）；"自我挑战"（戒肉食7天 GO)；更多工具
- 通用铁律：会员横幅永远在数据行下方、宫格上方；宫格 4 列，图标+文字；未登录态用渐变顶 + 大"登录/注册"
**UI 生成提示词**：
```
Mobile app profile page "我的", 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (social): top edit + settings icons, avatar + nickname "杰瑞" + ID badge, stats row 好友 0 / 关注 1 / 粉丝 0 / 访客 1. Dark member banner "开通解锁13大会员特权" + gold "立即开通" button. 4x2 icon grid: 我的钱包/幸运签到/认证/收益/任务/道具商城/背包/邀请赚钱. Toggle rows: 语音通话/视频通话/匹配接听 (off). List: 聊天设置/女神权益/贵族/我的成就.
Variant 2 (pet): teal gradient header with mascot + "HELLO~" bubble, avatar + "Hyacinth-xu" + ID, stats 胖豆 0 / 关注 4 / 粉丝 0 / 获赞 0, "添加我的爱宠" row, 3 functions （每日签到/胖豆商城/邀请好友）, tabs 动态/赞过/活动 + feed cards below.
Cute, colorful icons, clean.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"个人主页" + 下方双手机截图拼贴；标题 `💥设计赏析｜个人主页`

## 11 积分签到 Check-in
**定义**：每日签到领积分/券。
**设计要点**：7 天日历式签到；连续签到加成；积分商城入口；大按钮"立即签到"。
**UI 生成提示词**：
```
Mobile points check-in page, 9:19.5, Chinese UI.
Top card: "我的积分 1,280" big bold, button "兑换好礼".
7-day calendar row: past days gold checkmarks, today pulsing {主色} circle "今日", future gray.
Streak banner: "已连续签到 5 天，再签 2 天得 50 积分".
Big {主色} button "立即签到".
Below: 2-column grid of redeemable coupons (租房券 50元 / 保洁券).
Festive but clean, {背景色} background.
```
**黏土风封面**：卡片 A；标题 `💥设计赏析｜积分签到`

## 12 性别/偏好选择 Preference Select [实测：用户 8 张截图之 4 张性别选择封面]
**定义**：单选偏好页（如合租性别偏好、身份选择）。
**设计要点（8 版式全收录）**：
- A 横排大卡：左插画人物 + 右英文（Boy/Girl）+ 右下角黑圆角性别角标（男/女），选中整卡变黄底
- B MALE/FEMALE 竖卡：英文小字 + 头像，选中黄底 + 底部黑对勾圆点，未选中灰
- C 线稿头像卡：选中蓝色描边（我是男生/我是女生）
- D 圆形头像：选中项名字变蓝字
- E 灰调圆头像（侧脸）+ 粉渐变"下一步"CTA
- F 极简线条头像：近乎空白，线稿即内容
- G 吉祥物版：绿渐变底 + 圆形吉祥物 + 花名（甜酷GIRL/奇迹BOY），黑胶囊箭头按钮
- H STEP 步骤版：顶部"STEP 1"进度条 + chibi 大头照 + 绿色取景框（选中态），花名（辣妹Girl/酷盖Boy）
- 通用：顶部返回 + 步骤指示（2/4、跳过）；底部"下一步"大按钮，未选置灰
**UI 生成提示词**：
```
Mobile gender/preference selection page, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (horizontal cards): title "你的性别是？", two wide cards: left cartoon character illustration, right English word "Boy"/"Girl", small black rounded tag bottom-right "男"/"女". Selected card: full yellow #FFD400 background.
Variant 2 (STEP style): top "STEP 1" with progress bar, title "请选择你的性别", two chibi avatar portraits, selected one framed by green corner brackets + nickname below "辣妹Girl", bottom-right black pill button "下一步".
Clean white background, playful but tidy.
```
**黏土风封面**：黑底 + 白字"设计参考-" + 黄字"性别选择" + 下方双手机截图拼贴；标题 `💥设计参考｜性别选择`

## 13 集卡 Card Collection [实测：用户 8 张截图之 4 张集卡封面，支付宝集福卡式]
**定义**：活动集卡页（集齐兑换奖励）。
**设计要点（真实结构复刻）**：
- 顶部：IP 联名大标题（左返回）+ 右上"探福卡"文字入口
- 三个 pill 快捷入口：好友福榜 / 福气乐园 / 交换福卡
- 集卡奖励行："集齐主题全套福卡 有机会得礼品之一" + 奖品缩略图（3 个，带标签）
- 中央大卡：IP 主视觉大图；未获得态中央白字"未获得"；"稀有"渐变角标；下方小字"稀有卡不支持赠送/交换"
- CTA：奶黄渐变大圆角按钮"去集卡" / "找亲友要一张"
- 底部卡册：5 张小卡横滑 + 名称，稀有卡带角标
- 主题换肤：整套按 IP 换主题色（深蓝/紫/金红/浅蓝），结构不变
- 变体（兑红包版）：大标题"集卡兑红包 天天换好礼!!" + 卡片横排 + "奖品兑换区" + "我的奖品 >"入口
**UI 生成提示词**：
```
Mobile card-collection event page, 9:19.5, Chinese UI, festive.
Top: back arrow + IP co-brand title "XX联名" center + "探福卡" text button top-right.
Row of 3 pill buttons: "好友福榜" / "福气乐园" / "交换福卡".
Reward strip: "集齐主题全套福卡 有机会得礼品之一" + 3 prize thumbnails with labels.
Center: one large vertical card with original IP-style illustration (cute mascot scene), white text "未获得" overlaid, gradient "稀有" badge top-right, small note "稀有卡不支持赠送/交换" below.
Big cream-yellow gradient CTA button "去集卡".
Bottom: horizontal scroll of 5 mini cards with names below, rare ones badged.
Theme color {主题色} background with subtle pattern, sparkles.
All illustrations original, do not copy any existing IP characters.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"集卡" + 下方双手机截图拼贴；标题 `💥设计赏析｜集卡`

## 14 控件·天气/时间 Widget
**定义**：小组件（天气、时钟、倒计时）。
**设计要点**：圆角胶囊/方形；大数字+小图标；深色/浅色两版。
**UI 生成提示词**：
```
App widget design sheet, 9:19.5 canvas, Chinese UI.
Show 6 widgets in 2x3 grid on {背景色}:
1. Weather pill: sun icon + "28° 晴" + city.
2. Clock widget: big digital time "09:41" + date below.
3. Countdown card: "距看房还有 02:14:33" with progress ring in {主色}.
4. Mini calendar strip with today highlighted {主色}.
Dark-mode variants of 1 and 3 below (dark cards, white text).
Rounded {圆角}, soft shadows, clean.
```
**黏土风封面**：卡片 A；标题 `💥设计赏析｜天气控件`

## 15 付费订阅 Paywall [实测：用户 8 张截图之 4 张付费订阅封面]
**定义**：会员订阅页（付费墙）。
**通用骨架（8 屏验证）**：左上关闭 X → 主视觉（照片拼贴/吉祥物/大字标题三选一）→ 标题 + slogan → 权益列表 → 价格选项（2-3 档）→ 大 CTA → 底部小字（自动续费/条款/恢复购买）。
**设计要点（8 版式全收录）**：
- A 权益列表式：深色底，权益行（图标+标题+描述+右箭头），底部渐变大按钮"解锁全部功能"
- B 价格卡式：照片拼贴主视觉 + "XX Pro"渐变字；价格选项（连续包年/连续包月），选中绿描边 + "首充优惠"角标；渐变"立即订阅"；续费小字
- C 促销式：大标题 + 产品截图 +"新用户专享"角标；价格卡（1分钱体验/年度会员）；支付方式行；倒计时"限时活动"；金渐变"立即抢"
- D 三档+对比式：照片拼贴 + 评分星；Pro/Ultra 切换 pill；Benefits 对勾列表 + "Benefits Comparison >"；三档价格卡（选中金描边）；"CONTINUE"大按钮
- E 吉祥物式：渐变色吉祥物主视觉；"解锁无限访问 Pro"；绿对勾权益；价格选项（包年选中绿描边 + "立省 81%"角标）
- F 双档切换式：Premium/Premium+ 切换 pill；"Best value"角标价格卡（选中绿描边+对勾）
- G 写真促销式："免费写真集"荧光黄大字；emoji 开头权益列表；价格删除线对比；"SALE"角标；黄绿渐变"立即订阅"
- H 涂鸦式：涂鸦风标题 + 插画卡片；三档价格（Week/Month/3 Months)；"Start 3 days free trial"大按钮
- 促销三件套（至少用一件）：角标（首充优惠/立省81%/SALE/Best value）、倒计时、删除线原价
**UI 生成提示词**：
```
Mobile subscription paywall, 9:19.5, Chinese UI, dark premium style.
Top-left close "x".
Hero: photo collage (3 tilted photos) + big gradient title "XX Pro" + slogan "AI美颜、专属滤镜，全能的修图工具".
Benefits list with green checkmarks: 3 rows.
Pricing: 2 selectable rows — "连续包年 118元 仅0.32元/天" with "7天免费" tag, "连续包月 9元 15元" with "首充优惠" badge; selected row green border.
Big green-purple gradient button "立即订阅", tiny gray text "到期后会自动以15元/月开通续费，可随时取消".
Bottom: 使用条款 | 隐私政策 | 恢复购买.
Show ALSO a second variant: mascot hero (gradient cat mascot) + "解锁无限访问 Pro" + 3 green-check benefits + yearly/monthly options with "立省 81%" badge.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"付费订阅" + 下方双手机截图拼贴；标题 `💥设计赏析｜付费订阅`

## 16 引导页 Onboarding Coach Mark
**定义**：新功能/新页面的分步讲解浮层。
**设计要点**：全屏深色遮罩（60% 黑）；被讲解元素高亮（周围压暗）；气泡 tooltip 指向它（蓝底白字或黄底黑字）；一句口语化讲解 + 进度（"下一步 1/2"）；红色胶囊主按钮 + 描边"跳过"；每步只讲一件事；配吉祥物。
**UI 生成提示词**：
```
Mobile onboarding coach mark, 9:19.5, Chinese UI.
Background: app page dimmed with 60% black overlay, one white card highlighted (spotlight, no dim).
Speech-bubble tooltip pointing at the card: blue background white text "欢迎来到您的专属领地！这是您的身份标识～".
Bubble bottom row: text button "跳过引导" + red pill "下一步 1/2".
Cute pink cloud mascot peeking from bubble corner.
Show 3-step sequence as 3 phone frames: step 1/3, 2/3, 3/3 with progress.
Playful, clear, one concept per step.
```
**黏土风封面**：黑底 + 白色大字"引导页" + 白色短横线 + 右上斜体英文 "Introduction page'" + 下方手机截图；标题 `💥设计参考｜引导页`

## 17 卡片设计 Card Design [实测：用户 7 张截图之 4 张卡片设计封面 + 3 张第二批，新增]
**定义**：身份/人设/年度报告/营销类展示卡（MBTI、年度关键词、崽崽档案、简历、认证、商品、游戏）。
**通用骨架（15 屏验证）**：挂牌/档案式卡片（顶部挂绳/印章/条形码）→ 大字关键词 → 吉祥物/立绘 → 属性条/数据行 → 一句描述 → CTA。
**设计要点（15 版式全收录）**：
- A 星空加载：粉紫渐变底 + 星轨插画 + "正在聆听星星的指引"，仪式感加载页
- B MBTI 挂牌：粉色挂绳卡 + 条形码 + 印章；大字"INFP"；吉祥物 + 气泡"别害怕，我会给你加油~"；属性条（活力/感性Max/好奇Good)；黑 CTA"让我们一起开始吧"
- C 崽崽档案：紫底档案卡；吉祥物；toast"已展示在主页，火花豆+20"；信息行（生日/年级/能力值/崽ID)；"去做任务得装扮"；底部"晒晒我家崽崽"+"晒一晒"
- D 年度关键词：紫底；"佛系观察员"大黑字；3D 吉祥物；数据行（写评总数/被浏览数/写总字数）；"分享给好友/发布作品"双按钮
- E 职场 MBTI：绿底；"ENFJ 天生主角 天选C位，自带光芒"；吉祥物；2x2 数据卡（E-外向/热情洋溢…配具体数字）；"分享/保存图片/开启礼包"
- F 闲鱼简历：绿黑撞色；"要帮忙来找我"+"随时准备为您服务"；昵称 + "神秘人"标签；个人介绍；黄按钮"+我的副业"；"本人承诺真实"小字
- G 挂牌档案：蓝底；挂绳挂牌"ISTJ 守卫者"；吉祥物；"{ ISTJ-A 物流师 }"；"ISTJ的优点"描述；百分比（50%/76%/50%)；黑"返回"
- H ID CARD：顶部"ID CARD"英文；人物立绘；信息行（性别/年龄/日常喜好/特质）；黑"生成我的专属聊天人设"
- I 认证卡：蓝"主播认证" + 麦克风 3D，"完成主播认证，才可参与主播评级，解锁主播任务"，"去认证"；紫"歌手认证" + 唱片
- J 商品挂牌：吊牌形（孔+绳子），商品图，"OPPO A5"，✓IP69满级防水/✓6500mAh大电池/✓360°抗摔，大字"至高优惠309.85元"
- K 社交挂牌：吊牌形，"朝阳区钉子户"+"我的标签"，蓝怪兽吉祥物，"我/待邀请"头像位
- L 会员卡：蓝"优酷会员专区"，黄六边形心 3D，"咕咕卡"大字；粉红版"情人节限定"+"爱de咕咕卡"，爱心 3D
- M 表情包卡：浅色方卡（青/紫/黄/粉/蓝），"小酷坛子 轻酸不辣，张力拉满"+"添加"，吉祥物表情（已添加态变灰）
- N 课程卡：绿"萌芽期"，✓课程大纲/✓适合对象/✓学习目标，积木插画；黄"Level1"，橙✓，猴子插画，"共104节英语体系课"
- O 游戏卡：深色大图，"呆鸭杀 嘎嘎嘎，真心换真心"+"进入专区"；"桌球 展示一杆到底的实力"+"立即开玩"；"狼人杀 发言推理等你来聊"；"大富翁 完成小目标靠运气可以吗"
- 关键词公式：大字身份词（佛系观察员/天生主角/守卫者）+ 英文代码（INFP/ENFJ/ISTJ) + 具体数据（2%/1614个/3天）= 真实感
- 挂牌公式：吊牌孔+绳子 + 商品/人设 + 大字价格/身份 = 真实感
**UI 生成提示词**：
```
Mobile identity card design, 9:19.5, Chinese UI.
Show 3 variants side by side:
Variant 1 (MBTI badge): pink lanyard card with barcode + round stamp, huge letters "INFP", cute mascot, speech bubble "别害怕，我会给你加油~", attribute bars （活力/感性 Max/好奇 Good), one-line description, black CTA button "让我们一起开始吧".
Variant 2 (product hangtag): white hangtag with hole + string, phone image, "OPPO A5", checkmarks IP69满级防水/6500mAh大电池/360°抗摔， huge "至高优惠309.85元".
Variant 3 (game card): dark blue card with duck detective illustration in hat, "呆鸭杀" huge + "嘎嘎嘎，真心换真心", blue CTA "进入专区".
All text/characters original. Playful, collectible-card feel.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"卡片设计" + 卡片矩阵拼贴；标题 `💥设计赏析｜卡片设计`

## 18 发布页 Publish Page [实测：用户 8 张截图之 4 张发布页封面，新增]
**定义**：内容发布编辑页（笔记/动态/作品）。
**通用骨架（8 屏验证）**：顶部栏（取消/X + 标题 + 保存/发布）→ 媒体区（上传框/已选图/滤镜）→ 标题输入 → 正文输入 → 插入行（商户/地点/话题/物品）→ 关联行（话题#/商户/圈子）→ 可见范围 → 发布按钮。
**设计要点（8 版式全收录）**：
- A 笔记Tab式：顶部"记录一下/写游记/去提问"Tab（黄色下划线选中）；激励条"发一篇笔记，最高可得300蜂蜜（可抵现）"；相册缩略图横滑；底部黄"发布"
- B 发笔记式："取消/发笔记②/保存/发布"；虚线上传框"上传视频/照片"；标题"填写标题更容易上首页哦~"；插入行（商户/地点/菜品/物品）；关联话题#
- C 标签式："# 选择一个标签"；大正文区"记录这一刻…"；底部工具栏（相册/音乐/影视/emoji + 添加位置）
- D 动态式："记录一下吧，总有人懂你的每个瞬间"；+上传框；期待/位置/圈子/匿名行
- E 发布笔记式：图片 + "智能标题已生成"；#话题/@用户/互动组件；地点 chips；"公开可见"；"保存到相册"；红"发布笔记" + 存草稿
- F 新动态式：滤镜缩略图横滑；"#添加话题 获取更多曝光"；+上传框；添加地点/提醒谁看/谁可以看；红"发作品"
- G 极简式："想说你就多说点"；0/1000 计数；图片+上传框；圈子/合辑行；黄"发布"
- H 作品式：封面 + "编辑封面"；添加标题/作品描述；#话题/@朋友；地点；标签；"公开·所有粉丝可见"；高级设置；存草稿/发作品
- 通用铁律：顶部右"发布"按钮内容足够才点亮（灰→品牌色）；插入/关联行统一"图标+文字+>"；标题栏配激励文案（更容易被推荐/蜂蜜奖励）
**UI 生成提示词**：
```
Mobile publish/note editor page, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (note style): top bar "取消 / 发笔记 / 保存 / 发布"(orange pill). Dashed upload box "上传视频/照片" with camera icon. Title input placeholder "填写标题更容易上首页哦~". Body input with sample text. Row "插入 商户/地点 / 菜品 / 物品 >". Row "关联话题 #光合奇妙节 一起fun光芒！ x >". Row "关联商户/地点/菜品等 去选择 >".
Variant 2 (moment style): top "新动态" + red "发布". Input "分享新鲜事…". Horizontal filter thumbnails. "#添加话题 获取更多曝光 >". Upload box with +. Rows: 添加地点 / 提醒谁看 / 谁可以看（公开） each with icon + chevron.
Clean, airy, plenty of white space.
```
**黏土风封面**：黑底 + 白字"设计参考-" + 黄字"发布页" + 下方双手机截图拼贴；标题 `💥设计参考｜发布页`

## 19 人脸识别 Face Verification [实测：用户 8 张截图之 4 张人脸识别封面，新增]
**定义**：人脸识别/真人认证流程页。
**通用骨架**：标题 → 人脸框（取景框/虚线圆/渐变剪影）→ 三条件教学 → 正反例对比（✓/✗）→ CTA → 隐私说明。
**设计要点（8 版式全收录）**：
- A 示例教学："人脸识别示例" + 人物插画；三图（光线充足✓/平视手机✓/不遮挡面部✗)；"审核通过后才可接单"；蓝"开始人脸识别"
- B 身份验证：橙色警告条（新设备提醒）；四角取景框 + 虚线圆 + 人物；checklist 三行（本人操作/光线充足/按引导完成 ✓)；"您今天还有10次认证机会"；"取消/认证"双按钮
- C 英文极简："Ready to take a selfie?"；绿圈人脸线稿；三行说明配小图（红✗)；黑"Next"
- D 剪影式："请进行人脸识别认证"；虚线圆 + 红渐变人脸剪影；三图标（确保本人/光线充足/正面手机）；黑"开始人脸识别"
- E 认证中心："认证中心" + 隐私说明；"头像本人认证✓"；示例照片；权益行（优先推荐/认证标识/高阶隐私设置）；"认证攻略"四图对比（清晰五官✓/光线明亮✓/遮挡五官✗/脸占比小✗)；橙"立即认证，获得特权"
- F 真人认证："真人认证✓"徽标；虚线人形 + 标注（五官清晰/与头像照片一致）；三张反例 ✗；说明行；紫渐变"马上认证"
- G 支付验证："人脸识别验证身份" + "仅限本人操作"；3D 人物圆框；协议勾选"阅读并同意人脸验证协议"；红"刷脸验证"
- H 采集说明："为保障账户安全 需采集人脸信息核实身份"；加密说明行；人物圆框；三图标（正对手机/网络畅通/光线充足）；蓝"开始验证"
- 通用铁律：三条件永远是"光线/正对/不遮挡"；正反例用 ✓/✗ 对比图；隐私/加密说明必备（过审）；CTA 用蓝/黑/品牌色大按钮
**UI 生成提示词**：
```
Mobile face verification page, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (tutorial): title "人脸识别示例", cute 3D character illustration in blue circle, white card with 3 mini illustrations: 光线充足 (blue check) / 平视手机 (blue check) / 不遮挡面部 (red x), note "如果认证不通过，请按照提示多尝试几次", blue button "开始人脸识别".
Variant 2 (verification): title "身份验证", orange warning banner "检测到您正在使用新的设备，为确保账户安全，请先完成身份验证。", face frame (blue corner brackets + dotted circle + person illustration), checklist card with 3 green-check rows: 1、本人操作； 2、环境光线充足； 3、按照引导完成验证；, note "您今天还有10次认证机会", two buttons "取消" outline + "认证" blue.
Trustworthy, clean, friendly.
```
**黏土风封面**：黑底 + 白字"设计参考-" + 黄字"人脸识别" + 下方双手机截图拼贴；标题 `💥设计参考｜人脸识别`

## 20 排行榜单 Ranking [实测：用户 7 张截图之 4 张排行榜单封面，新增]
**定义**：活动/游戏排行榜页。
**通用骨架（8 屏验证）**：标题 + 规则入口 → （个人排名卡）→ 榜单切换 Tab（昨日/今日、周榜/总榜、朋友榜/全服榜）→ 前三领奖台 → 4-N 名列表 → 底部我的排名条。
**设计要点（8 版式全收录）**：
- A 小镇经营：蓝底；"小镇经营奖励"+"规则"；个人信息卡（头像/昵称/等级/排名/金币)；"等级奖励/经营排行榜"Tab；"前10名可得大奖 iPhone 16 Pro"+"提醒我"；领奖台 1st/2nd/3rd；列表（4/5/6名+等级+金币）
- B 战力榜：蓝渐变；"清凉战力榜"+奖励说明；"昨日榜单/今日榜单"切换；领奖台（TOP1粉/TOP2蓝/TOP3绿）；列表 04-09名（头像+分）；底部"未上榜 我的排名"蓝条
- C 乱涂挑战：紫底；"乱涂挑战"+"排名奖励"；前三卡片（名次+头像+进度）；列表行（名次+头像+名+进度+"查看阵容>");底部 BACK/挑战/追辑
- D 学习榜：米黄；奖杯标题"排行榜"；倒计时"每周结算倒计时：5天08时48分"；"段位/学习/魅力/校友"Tab；前三徽章卡（学习力 K 数）；列表 4-10名；底部"1w+ 我的排名 0"
- E 勋章排行：青底；"哈啰挑战赛 勋章排行"涂鸦大字；前三（251/249/243枚）；列表 4-7名（枚数）
- F 充能榜：绿底；"充能榜/月票榜"Tab；个人信息（20/本月排名）；"月榜/总榜"；领奖台"虚位以待 快抢沙发"；吉祥物；"去充能"绿按钮
- G 冲榜赢大奖：蓝底；"冲榜赢大奖"+时间；奖品展示；"周榜/总榜"切换；领奖台（星光值大数字）；列表 4/5/6名；底部"冲榜 本周175星光值"+"去分享"
- H 朋友榜：双 Tab"朋友榜/全服榜"；倒计时；"本周/上周"；领奖台（"虚位以待 叫朋友一起玩"/第1关）；"和朋友一起玩"列表 + 去分享/去冲榜
- 领奖台铁律：1/2/3 名高低错落，冠亚季配色区分；无人时写"虚位以待 快抢沙发"（占位文案）
- 倒计时/结算时间必备；"提醒我"/"去冲榜"/"去充能"CTA；底部永远是"我的排名"条（未上榜也显示）
**UI 生成提示词**：
```
Mobile ranking leaderboard page, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (battle): blue gradient background, title "清凉战力榜" + subtitle "挑战单局最高纪录、赢大奖", toggle pills "昨日榜单/今日榜单". Podium: TOP 1 (pink, tallest, avatar + name + score 2418), TOP 2 (blue, 2278), TOP 3 (green, 2140). List rows 04-09: rank number + avatar + nickname + score. Bottom blue bar "未上榜 我的排名 0".
Variant 2 (learning): cream background, trophy title "排行榜", countdown "每周结算倒计时：5天08时48分", tabs 段位/学习/魅力/校友. Top-3 badge cards with 学习力 numbers (4.26K/7.08K/2.92K). List rows 4-10: rank + avatar + name + 学习力. Bottom bar "1w+ 我的排名 0".
Festive, competitive, clear hierarchy.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"排行榜单" + 下方双手机截图拼贴；标题 `💥设计赏析｜排行榜单`

## 21 PK组件 PK Battle [实测：用户 6 张截图之 3 张PK组件封面，新增]
**定义**：双人/双队对战组件（直播PK、游戏对战、投票PK）。
**通用骨架**：红方 vs 蓝方 → 中央 VS 大字 → 比分/票数条 → 胜/败徽章 → 倒计时。
**设计要点（10 版式全收录）**：
- A 开启PK：红蓝两方（曲目/暂无歌曲），头像 + 先唱/后唱标签，中央PK徽章，"PK 3V3 GAME"
- B 胜利：紫底，"胜利"涂鸦大字，胜方/败方徽章（胜/败）
- C 比分条：粉 133273 vs 蓝 48087，渐变比分条
- D 积分：蓝方"积分1000（+16)" vs 红方"积分992（-8)"，头像 + 称号（勇猛果断的加冈/天真烂漫的梅雅），中央VS
- E 支持：顶部"剩余支持机会1次"，红方"办公室裁判" vs 蓝方"居家播报员"，"支持TA"按钮 + 中央PK
- F 匹配：红方"我" vs 蓝方"?"，"匹配中…"
- G 骰子：蓝vs红骰子吉祥物，"与全世界的散友或是好友一同较量一下实力吧"
- H 橙蓝波浪：橙vs蓝波浪形，头像，中央金色VS
- I 主播PK：六边形头像框（蓝/粉），昵称，中央VS，倒计时"1:54"，比分条
- J 主持PK：紫底，"主持PK 0s"，双方票数（8.7w vs 1.8w），前三贡献头像，"排行榜"按钮
- 通用铁律：红vs蓝是PK的默认配色语言；中央VS永远最大；比分条用渐变表示比例；胜/败徽章盖在头像角上
**UI 生成提示词**：
```
Mobile PK battle component, 9:19.5, Chinese UI, dark background.
Top: red team card (avatar + nickname + song "《半岛铁盒》" + tag 后唱） vs blue team card (avatar + 暂无歌曲 + tag 先唱）, center hexagonal "开启PK" badge.
Middle: full-width score bar, pink 133273 vs blue 48087, gradient.
Bottom: blue panel "积分 1000（+16)" with avatar + title "勇猛果断的加冈" vs red panel "积分 992（-8)" with avatar + "天真烂漫的梅雅", big gold "VS" in center.
Second variant: purple host PK panel, "主持PK 0s", two vote counts 8.7w vs 1.8w with VS, top-3 contributor avatars, "排行榜" button.
Energetic, neon, competitive.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"PK组件" + 对战截图拼贴；标题 `💥设计赏析｜PK组件`

## 22 会员卡片 Member Card [实测：用户 6 张截图之 3 张会员卡片封面，新增]
**定义**：会员等级展示卡（V等级/SVIP/贵族）。
**通用骨架**：大字等级（V4/Lv5/SVIP12）+ 会员名 → 3D 徽章/宝石 → 有效期/成长值 → 进度条 → CTA。
**设计要点（20 版式要点全收录）**：
- 等级命名：V1-V7 / Lv1-Lv8 / SVIP12-15 / 铂金/金卡/黑金/钛金/白银/星钻/星辰
- 配色按等级：银（铂金/白银）/ 金（金卡/黄金）/ 紫（星钻/星辰/SVIP) / 黑（黑金/至尊）
- 3D 徽章三选一：盾徽 / 钻石 / 皇冠，永远放卡片右侧
- 状态三态：当前（亮+有效期）/ 未达成（暗+未解锁+还差多少）/ 可升级（进度条+去解锁）
- 进度条文案："成长值需达到20000" / "本月成长值满900，继续加油" / "648/1200 消费分"
- 特权展示：6 个图标横排（锁定时灰+锁），"开通会员，享N项专属特权"
- CTA："立即开通"（金/紫大按钮）/ "去解锁" / "查看福利"
- 个人版：头像 + 昵称 + 到期日 + "尊享N项会员特权" + 进度条
- 皇冠/钻石等 3D 元素是"贵气感"的核心，不可省略
**UI 生成提示词**：
```
Mobile membership level cards showcase, 9:19.5, Chinese UI, black background.
2x4 grid of 8 cards, each: big level text (V4/Lv5/SVIP12/V7) + member name （铂金会员/创作等级/荣耀会员） + 3D badge (shield/diamond/crown) on right + progress bar + CTA.
Variants: V4 铂金会员 silver with shield badge "当前等级"; V3 金卡会员 gold; V6星钻等级 purple "未达成" with diamond + "立即开通"; Lv5 创作等级 black with stars; V7 black "未解锁，里程值需达到1100" with black diamond; 星辰会员V4 purple "有效期至2024年8月2日" + growth progress 103645/100000; SVIP12 pink vs SVIP15 black with crowns.
Luxurious, 3D badges, clear locked/unlocked states.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"会员卡片" + 卡片矩阵拼贴；标题 `💥设计赏析｜会员卡片`

## 23 按钮/标签 Button & Tag [实测：用户 7 张截图之 3 张按钮/标签封面，新增]
**定义**：营销按钮/标签样式库（30 款）。
**通用铁律**：胶囊形为主；文案永远是动词（领取/开启/抢购/抽奖/收下/助力）；渐变 + 描边 + 一个小装饰（星星/眼睛/鼠标手/闹钟）；角标（x1/1人助力/值回票价/剩余2次）。
**设计要点（15 类全收录）**：
- A 紫渐变胶囊："开心收下"，描边字/白字 + 星星点缀
- B 黑底荧光：黑底 + 荧光描边，"邀请同学助力获得"/"免费开盲盒"，右上小标签"值回票价"
- C 果冻蓝：果冻质感"点击进入直播间" + 闹钟装饰；"马上抽奖"青绿斜切
- D 粉红："立即领券"粉红胶囊；"去看看>"异形
- E 黄黑撞色：黄底黑字"邀请同学助力" + 眼睛；绿"领权益" + 粉 x1 角标
- F 描边大字：紫底"马上领取"描边字；橙"一键领取" + 粉箭头
- G 奶油：奶油底"立即开启"；蓝"去看看>"
- H 盲盒黄：黄"立即抢购" + 箭头圆；"开盲盒 剩余2次抽奖机会" + 鼠标手
- I 红："开心收下"红渐变；"真朋友 听歌匹配度≥50%"
- J 黄描边字：黄"立即开启"；"收下"黄底 + 黑描边字
- K 黑底荧光字："开始摸鱼"/"Try it now"荧光描边字
- L 果冻："查看奖励"蓝果冻；橙"邀请好友助力" + 绿角标"1人助力"
- M 抽奖红：红"免费抽（有几率获得拍拍币~)" + x1黑角标；粉"立即抽盲盒" + 黄条幅"运气爆棚！送你1次抽盲盒机会"
- N 粉橙："立即参与"粉；橙"领取福利" + 箭头圆
- O 大字黄：黄底"立即出拳"大描边字
**UI 生成提示词**：
```
Marketing button style sheet, black background, 9:19.5 canvas, Chinese UI.
3x5 grid of 15 capsule buttons, each different style:
1. Purple gradient "开心收下" with white outline text + sparkles.
2. Black with neon outline "免费开盲盒" + small yellow tag "值回票价" top-right.
3. Jelly blue "点击进入直播间" with alarm clock icon.
4. Pink gradient "立即领券".
5. Yellow with black text "邀请同学助力" + cartoon eyes on top edge.
6. Green "领权益" + pink "x1" badge.
7. Purple "马上领取" with white outline text.
8. Orange "一键领取" + pink arrow.
9. Yellow "开盲盒 剩余2次抽奖机会" + cursor hand icon.
10. Black "开始摸鱼" with neon gradient outline text.
11. Blue jelly "查看奖励".
12. Orange "邀请好友助力" + green badge "1人助力".
13. Red "免费抽（有几率获得拍拍币~)" + black "x1" badge.
14. Pink "立即抽盲盒" + yellow ribbon "运气爆棚！送你1次抽盲盒机会".
15. Yellow "立即出拳" with big black-outline text.
Glossy, juicy, high click-appeal.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"按钮/标签" + 按钮矩阵拼贴；标题 `💥设计赏析｜按钮/标签`

## 24 秒杀/拼团 Flash Sale & Group Buy [实测：用户 7 张截图之 4 张秒杀/拼团封面，新增]
**定义**：秒杀/拼团活动页。
**通用骨架（8 屏验证）**：暖色头图（大字标题 + 倒计时 + 吉祥物）→ 时间Tab/分类Tab → 商品列表（图 + 名 + 券 + 价格三件套 + 抢按钮）。
**设计要点（8 版式全收录）**：
- A 秒杀超级桶：粉红头"秒杀超级桶 狂补破价"；"整点秒杀 超级狂补"；商品卡（19点/20点/21点秒杀）；"官方补贴108元"；"秒杀价¥68"+"抢>"
- B 限时秒杀：红头"限时秒杀"+"正品保障 全场包邮 天天一元抢"；"抢购中 仅剩09:39:38"；分类Tab；商品（直降¥25，¥49.9→¥24.9秒杀价+"抢>")
- C 双11：红头"双11真5折"+"距结束15:49:30"+日历；"超值购·万人团"；商品（券后价¥240+"抢"，"已补12元")
- D 天天低价：橙头"天天有低价 低至9.9"；"无需领券 立享优惠"；"9.9元 惊喜价打车券"；"输入起终点 查看优惠"；"省钱套餐限时购 8.5折"；"马上抢购>>"；"邀好友 得好礼"
- E 省钱攻略：红头"省钱攻略 省到就是爽到"；吉祥物；"神券福袋 一单回本"；"限时抢购 最高省158元"；券宫格（¥18/¥12/¥3)；"¥0.18 含158元神券"+"去抢购"
- F 春日大放价：粉头"会员2周年 春日大放价"；"开卡抽赠好礼 100%有奖"；"年卡会员 ¥88（原价¥228)"；"限时优惠00:29:37"；"¥88立即开通"；支付方式
- G 一起拼：红头"一起拼 更便宜"+"等1000+人已成团"；"发起拼团>>24小时内邀人拼单>>成团发货"；商品（超值购 2人团，成团价¥19.93+"抢")
- H 半价券：粉红头"20元半价券 周周抢"；时间Tab（9:00抢购中/11:00未开始…）；券卡（¥20满40可用）；"本周大牌 超值折扣"（买1送1，5.0折+"立即抢购>")
- 通用铁律：头图永远暖色（红/粉/橙）；大字标题 + 倒计时缺一不可；价格三件套（原价删除线/券后价/秒杀价红）；"抢>"按钮永远红色；"已补N元"/"官方补贴"信任状
**UI 生成提示词**：
```
Mobile flash-sale page, 9:19.5, Chinese UI.
Top: red-pink header with huge white text "限时秒杀" + "正品保障 全场包邮 天天一元抢", countdown "抢购中 仅剩09:39:38", cute mascot.
Category tabs: 超级秒杀/热卖/食品水饮/个护美妆/数码家电.
Product list, each row: product image, name "雪玲妃烟酰胺樱花身体乳500g", "已售493件", price trio: ¥49.9 strikethrough → 直降¥25 → red "¥24.9 秒杀价" + red "抢>" button.
Second variant (group buy): red header "一起拼 更便宜" + "等1000+人已成团", steps "发起拼团 >> 24小时内邀人拼单 >> 成团发货", product rows with "超值购 2人团" tag + "成团价¥19.93" + red "抢" button.
Urgent, hot, price-focused.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"秒杀/拼团" + 双手机截图拼贴；标题 `💥设计赏析｜秒杀/拼团`

## 25 顶部视觉 Top Visual [实测：用户 8 张截图之 3 张顶部视觉封面，新增]
**定义**：App 首页顶部 banner/头图区（第一屏上半）。
**通用骨架**：导航栏（返回+标题+图标）→ 大标题（描边字/渐变字）→ 一句 slogan → 吉祥物/插画 → 功能入口（Tab/宫格/搜索框）。
**设计要点（11 版式全收录）**：
- A 同城服务：蓝渐变顶；"同城服务·北京市"；大字"物品急送 琐事帮忙"+"一键托付 极速接单"；快递车插画；Tab（帮取/帮送/帮我买/万事帮/我的订单）；地址输入行
- B 挑战赛：蓝绿顶；"哈啰挑战赛"；30KM 徽章；"我的挑战赛 0 进行中"/"我的勋章 16 已获得"；Tab（全部/星座系列/骑行运动会…）
- C 深圳服务："深圳· 推荐/附近"；"新用户专享福利"+"立即查看>"；人物插画；搜索框"户外设备租赁"；宫格（日常保洁/保姆月嫂/放心搬家/家电维修…）
- D 精选主理人：青绿顶；"精选主理人 SELECTED OWNER-PRINCIPAL"+"社区排行榜"；吉祥物；"杭州周末玩俱乐部"+"历史举办了115场活动"；slogan"户外找搭子，快乐供电所"
- E 恋爱人格："测测你的恋爱人格"+"获取专属恋爱方案"；"立即测试>"；黄鸭吉祥物；搜索框；功能卡（追爱键盘/知知老师）
- F 萌宠生活馆："萌宠生活馆"+"宠物服务来宠物之家"；柴犬；搜索框"成都·输入套餐名称"；功能卡（宠物服务/上门宠托/闪电送宠）
- G 滴滴顺风车：绿顶；"乘客/车主/车生活"；大字"欢迎使用 滴滴顺风车"；地图；常用车点
- H 高铁管家："高铁管家 铁定有票"渐变大字；"出票方案全 出行有保障"；吉祥物开箱；"免费领7元火车票红包+VIP光速抢票券！"
- I 盲盒："推荐/潮玩/模玩/卡牌/谷子"Tab；"开箱抽得心仪盲盒"；开奖条；"夏日光年 梦想启航"+"立即前往"
- J 附近活动："附近活动 新玩法，拼好玩！"；Tab（新年打卡/全部/密室/剧本杀…）；活动卡（周六|环骑青山湖…+"上车"）
- K 闲鱼公益："闲鱼公益宝贝"+"卖闲置也能做公益"；鱼吉祥物；流程"1发布宝贝>2买家购买>3交易成功>4公益捐赠"；"累计已发布318845个公益宝贝"；"累计捐赠金额120.6万元"
- 通用铁律：底色永远渐变（蓝/绿/粉）；大标题用描边字或渐变字；吉祥物/插画占右半屏；slogan 一句话说清价值；功能入口紧跟其下（Tab/宫格/搜索三选一）
**UI 生成提示词**：
```
Mobile app home top visual, 9:19.5, Chinese UI.
Show 2 variants side by side:
Variant 1 (city service): blue gradient header, nav "同城服务·北京市", huge bold title "物品急送 琐事帮忙" + subtitle "一键托付 极速接单", delivery truck illustration on right, tab row （帮取/帮送/帮我买/万事帮/我的订单）, address input rows below.
Variant 2 (pet): light green header, huge title "萌宠生活馆" + subtitle "宠物服务来宠物之家", cute Shiba illustration, search bar "成都 · 输入套餐名称" with black search button, 3 function cards （宠物服务/上门宠托/闪电送宠） with illustrations.
Big outlined/gradient titles, mascot on right half, one-line slogan, functional entries below.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"顶部视觉" + 头图拼贴；标题 `💥设计赏析｜顶部视觉`

## 26 TAB切换 Top Tabs [实测：用户 8 张截图之 4 张TAB切换封面，新增]
**定义**：顶部横滑 Tab 切换条（非底部导航）。
**选中态四手法**：胶囊 / 下划线 / 背景块 / 异形标签，未选中一律灰字。
**设计要点（24 条全收录）**：
- 胶囊类：绿胶囊"周末游🔥🔥🔥"+"限时福利倒计时"；黑胶囊"全部"+绿剪刀；蓝胶囊"出行榜"；黄标签"特价出行"+笑脸
- 下划线类：黑字+黄下划线"大家都在买"；黑大字+红下划线"收藏"；蓝字+蓝下划线"余票监控"（+红角标"成功率高")；"火车票"黑大字+黄下划线；"蔬菜水果"+绿波浪线；"全部"+黄绿波浪线
- 背景块类：灰底块"全部"+红心；黄块"推荐 猜你喜欢"（+副标题）；黄块"旅行灵感 甄选旅行好货"；绿块"推荐"
- 异形类："住家 生活起居"白卡凸起；"合租"黄标签凸起（顶部小房子插画）；"宠物专送"白卡凸起+橙下划线+"促"角标
- 大字类：黑大字"消息"+黄下划线（+红点）；"北京·"+黑点 vs "必游榜>"黄渐变
- 图标类："NEW 上新"黑圆+字；紫渐变"礼遇/时尚"+图标
- 装饰：🔥/波浪线/角标（促/成功率高）/副标题（猜你喜欢/短途好去处）
- 通用铁律：选中黑字 + 未选中灰字是底线；至少有一种装饰（下划线/胶囊/角标）；可横滑时末尾露半个表示可滑
**UI 生成提示词**：
```
Mobile top tab bar style sheet, black background, 9:19.5 canvas, Chinese UI.
4x6 grid of 24 tab bars, each different selected-state style:
Row 1: green capsule "周末游🔥🔥🔥" with countdown "限时福利：00:00:40" / black text "大家都在买" with yellow underline / "药品管理" black with blue underline vs gray "用药计划" / gray block "全部" with red heart.
Row 2: big black "消息" with yellow underline + red dots / "NEW 上新" black circle / purple gradient "礼遇" with gift icon / big black "收藏" with red underline.
Row 3: black capsule "全部" with green scissors vs gray "喂猫/喂狗/喂鸟" / yellow block "推荐 猜你喜欢" / yellow tag "合租" popped up with tiny house illustration.
Row 4: blue text "余票监控" with blue underline + red badge "成功率高" / "火车票" big black with yellow underline / green wave "领优惠" vs black "用里程" / white popped card "宠物专送" with orange underline.
Selected = black text + one decoration (capsule/underline/block/tag), unselected = gray text.
Playful, varied, high contrast.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"TAB切换" + Tab条拼贴；标题 `💥设计赏析｜TAB切换`

## 27 医疗/健康 Medical & Health [实测：用户 7 张截图之 4 张医疗/健康封面，新增]
**定义**：医疗健康类 App 页面（AI问诊、健康档案、问医生、保障）。
**通用骨架**：信任状（医生/三甲/认证）→ 数据卡（指标+记录按钮）→ 功能入口 → 隐私提示。
**设计要点（8 版式全收录）**：
- A AI解读：Tab（对话/发现）；"AI智能解读报告"；行（拍照/上传照片/上传PDF文件 + 去拍照/去上传）；底部输入"有什么健康问题需要问我吗~"；底部Tab（首页/健康甄选/AI健康管家/医保/我的）
- B 健康档案：用户头像；"运动健康AI·步数"曲线图（周三-周二）；"近7日步数偏少，多走路，健康快乐不迷路！"；Tab（就医资料夹/健康史/用药计划/我的药箱）；"门诊病历/门诊处方/出院记录"+"点击上传"；蓝条"隐私隐藏"
- C 健康助手："夸克健康助手"；医生插画；气泡"Hi，我是你的健康助手 请问有什么健康问题吗？"；"每日谣言粉碎机"（对/不对投票）；"健康科普"卡（指甲侧面倒刺…）；底部功能（症状自查/报告解读/在线问诊/AI自测）
- D 问医生："问医生/问诊记录"；"用药咨询 指导选药、用药"+"极速问诊 看病、指导治疗"双卡；信任状（执业药师/三甲医院医生/平均30秒回复）；科室宫格（呼吸内科/耳鼻喉科/儿科/消化内科/妇产科/皮肤性病科/泌尿男科/心血管内科/内分泌科/神经内科/中医科）；"选药贴士"（眼耳鼻喉/两性健康/胃肠肝胆…）；药品列表
- E 健康档案2：用户"用户215822… 本人 女 0岁"；"档案完整度15%"；"六维健康测评"；"健康画像"（人体3D+定制体检套餐）；部位Tab（头部/颈部/胸部）；"健康记录"（问诊记录/用药记录/体检报告/挂号记录）
- F 补充保障："补充保障专区·宁波"；"家庭保障/我的/家人/订阅"；三圆环（补充医保/基础医保/重疾保障 未激活）；"保障程度低 0%"；"全家无忧保（0免赔）"+"去看看"；"康医保（普惠版）"
- G 健康监测："健康监测/体检报告/就医记录/健康小结/生活习惯"Tab；"基础数据"（18.3 BMI/170 身高/53 体重 +记录）；"血糖信息 3.9-6.1"；"血压信息 90-140/60-90"；"心率数据 --"
- H 京东健康："JDH京东健康"；搜索框；Tab（推荐/正品好药/医疗器械/保健滋补/到店服务）；"在线问医生/京东大药房"双卡；"秒问京医 30秒极速接诊"；功能宫格（家庭医生/找医生/宠物医院/按方抓药）
- 通用铁律：配色永远医疗绿/蓝（信任感）；信任状三件套（执业药师/三甲/国家认证）；数据卡 = 指标大字 + "+记录"按钮；隐私提示必备（蓝条/小字）
**UI 生成提示词**：
```
Mobile medical health app pages, 9:19.5, Chinese UI, medical green/blue palette (#00C389 / #2E9BFF).
Show 2 variants side by side:
Variant 1 (AI health assistant): top nav "健康助手", doctor illustration, chat bubble "Hi，我是你的健康助手 请问有什么健康问题吗？", "每日谣言粉碎机" card with 对/不对 vote buttons, "健康科普" cards row （症状自查/报告解读/在线问诊/AI自测）.
Variant 2 (health record): "健康档案" title, user row, "运动健康AI·步数" card with 7-day step line chart, "近7日步数偏少，多走路，健康快乐不迷路！", tabs （就医资料夹/健康史/用药计划/我的药箱）, upload rows （门诊病历/门诊处方/出院记录 + 点击上传）, blue privacy bar.
Trustworthy, clean, data-forward.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"医疗/健康" + 双手机截图拼贴；标题 `💥设计赏析｜医疗/健康`

## 28 异形弹窗 Irregular Popup [实测：用户 3 张异形弹窗封面，新增]
**定义**：中央悬浮的营销弹窗，容器形状不规则（区别于底部弹窗的底部升起操作面板）。
**通用骨架**：异形容器（3D质感）→ 大字标题（金额/权益）→ 副标题 → 胶囊 CTA → 装饰元素顶出容器。
**设计要点（27 款全收录）**：
- 形状即内容：罐子装券（50元券/88小时会员）/ 卷轴表遗憾（"很遗憾！你还没集齐5个字群"）/ 云朵表未创建（"还未创建宠物"）/ 拍立得（拍拍乐公仔兑换券）/ 扭蛋机（猫爪）/ 盲盒（火车票盲盒）/ 圣诞树（2023迎新特惠）/ 招财猫（吞金兽领920元红包）/ 中国结挂饰（冲66)
- 大字永远是金额或权益："88小时会员"/"50元券"/"920元红包"/"123元现金"/"0.66元"/"¥176"/"3999元现金红包"
- CTA 胶囊按钮："知道了"/"立即领取"/"马上领钱"/"免费开盲盒"/"去挑战"/"开始学习"
- 装饰顶出：星星/挂饰/书本/猫头鹰从容器顶部探出
- 双按钮版："就它了！/重新换一张"（火车票盲盒）；"查看详情/我知道了"
- 券版：三券横排（¥20机票/¥50门票/¥20酒店），"开启白银之旅"
- 抽奖版："¥50/¥118/¥220"三档，"再抽一次"，"离大奖仅一步之遥"
- 通用铁律：形状先讲故事，文字只讲金额；一个弹窗只讲一件事；CTA 永远胶囊大按钮
**UI 生成提示词**：
```
Irregular-shaped marketing popup designs, black background, 9:19.5 canvas, Chinese UI.
3x3 grid of 9 popups, each with a different irregular 3D container:
1. Pink glass jar with "50元券" ribbon + red capsule "立即领取".
2. Purple scroll with "很遗憾！你还没集齐5个字群 集齐后再来开奖赢豪礼~" + orange "知道了".
3. White cloud with "还未创建宠物 需要先创建宠物形象，才可以抽取盲盒" + black "我知道啦".
4. Pink polaroid ticket "拍拍乐公仔 兑换券 1234567 8901234".
5. Cat-paw gashapon machine with colorful capsules.
6. Christmas tree with "2023迎新特惠" ribbon + green "立即查看".
7. Lucky cat with "吞金兽邀你 领920元红包" + red "领".
8. Train ticket blind box "智行火车盲盒 抽到爽再付款" + black "免费开盲盒".
9. Purple "离大奖仅一步之遥" with ¥50/¥118/¥220 three tiers + "再抽一次".
Big amount/benefit text, capsule CTA, decorations popping out of container top. Juicy 3D, festive.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"异形弹窗" + 弹窗矩阵拼贴；标题 `💥设计赏析｜异形弹窗`

## 29 表单输入 Form Input [通用：高频刚需，非实测]
**定义**：输入框/选择器/开关/步进器。
**通用骨架**：标签 → 输入区（左图标+占位文案+右清除/眼睛）→ 校验文案 → 提交按钮。
**设计要点**：
- 聚焦态：边框变主色 + 轻微上浮，失焦恢复
- 错误态：红边 + 红字一句人话（"手机号不对，再看看"），不甩错误码
- 禁用态：灰底 + 灰字
- 开关：iOS 式，选中主色
- 步进器：- 1 + 胶囊组
- 提交按钮：内容为空时禁用灰，填完变主色（状态诚实）
**UI 生成提示词**：
```
Mobile form inputs, 9:19.5, Chinese UI, cute clay style.
Show: text input with label "手机号", focused state with orange border; error state "验证码不对，再试一次" in red; toggle switch on/off; stepper "- 1 +"; submit button disabled gray vs enabled orange.
States: default / focused / error / disabled.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"表单输入"；标题 `💥设计赏析｜表单输入`

## 30 空状态与异常页 Empty & Error [通用：高频刚需，非实测]
**定义**：无内容/加载失败/网络错误/404。
**通用骨架**：吉祥物（沮丧/睡觉）→ 一句话安慰 → 一个 CTA。
**设计要点**：
- 文案说人话："这里空空如也" / "网络开小差了" / "页面去旅行了"
- 必须有一个 CTA："去逛逛" / "重新加载" / "回首页"
- 空状态和错误页视觉区分：空=浅色吉祥物，错误=深色+重试
- 禁止只有文字的"暂无数据"（反模式 #6）
**UI 生成提示词**：
```
Mobile empty and error states, 9:19.5, Chinese UI, clay style.
3 panels: empty (sleeping mascot + "这里空空如也" + orange CTA "去逛逛"); network error (dizzy mascot + "网络开小差了" + "重新加载"); 404 (mascot with map + "页面去旅行了" + "回首页").
One mascot + one line + one CTA each.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"空状态"；标题 `💥设计赏析｜空状态与异常页`

## 31 订单卡片 Order Card [通用：高频刚需，非实测]
**定义**：订单/账单列表卡。
**通用骨架**：状态标签（色块）→ 商品/服务行（图+名+规格）→ 金额行 → 操作按钮。
**设计要点**：
- 状态色：待付款橙 / 进行中蓝 / 已完成灰 / 退款中紫
- 金额右对齐，加粗；实付标红
- 操作按钮按状态：待付款（取消订单/去支付）/ 已完成（再来一单/评价）
- 时间线：重要订单加"已接单→进行中→已完成" mini 进度
**UI 生成提示词**：
```
Mobile order cards, 9:19.5, Chinese UI, clay style.
3 cards: 待付款 (orange tag, "取消订单" outline + "去支付" orange), 进行中 (blue tag + mini timeline), 已完成 (gray tag, "再来一单" + "评价").
Each: product row (thumb + name + spec), amount right-aligned bold, real pay in red.
```
**黏土风封面**：黑底 + 白字"设计赏析-" + 黄字"订单卡片"；标题 `💥设计赏析｜订单卡片`
