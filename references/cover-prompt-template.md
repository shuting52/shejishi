# 封面生图提示词模板

> v2 起：6 种版式的"一键复制卡"已收录在 [prompt-cards.md](prompt-cards.md)，优先用卡片。
> 本文件保留基础模板，供需要自定义版式时使用。

把 `{关键词}` 替换成组件名（如"搜索历史"），直接投喂图片生成模型。
中文描述给自己看，英文 prompt 给模型，准确率更高。

## 中文描述
UI 设计干货笔记封面：纯黑背景。左上角一个白色描边空心圆角胶囊，里面白字写"设计细节"；右上角白色小字"-UI/UX"。画面中央大标题，白色粗黑体"设计赏析-"后面跟明黄色（#FFD400）大字"{关键词}"。标题下方是 2 列 4 行共 8 张手机 App 界面截图拼贴，圆角卡片，全部展示"{关键词}"相关的界面。底部中央小字署名水印。整体风格：大字报式、干货密集、高对比。

## English prompt（投喂模型用）
```
Xiaohongshu UI design tutorial cover, pure black background (#000000).
Top-left: a white outline pill-shaped badge with white Chinese text "设计细节".
Top-right: small white text "-UI/UX".
Center: big bold headline, white Chinese characters "设计赏析-" followed by bright yellow (#FFD400) large Chinese characters "{关键词}".
Below headline: a 2-column x 4-row grid of 8 rounded-corner smartphone app UI screenshots, all showing "{关键词}" interfaces, collage style.
Bottom center: small white watermark signature text.
Style: bold poster typography, dense informative layout, high contrast, flat design, no photo of people.
Aspect ratio 3:4.
```

## 变体：原创改版项目封面
```
Light beige background. Top-left dark pill badge with "置顶".
Center: huge bold Chinese characters "{概念词}" with subtitle "{项目名}体验改版原创设计".
2-3 smartphone mockups showing the redesigned app screens, floating at an angle.
Top-right small watermark "@{你的署名}".
Clean, premium, minimal style. Aspect ratio 3:4.
```

## 注意事项
- 生图模型对中文大字容易写错字：标题字建议后期用设计工具叠加，不要全靠生图。
- 截图矩阵里的 8 张图用真实 App 截图拼贴效果最好，AI 生成的假界面经不起细看。
- 黄色关键词色值锁死 #FFD400，全系列统一。
