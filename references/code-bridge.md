# 代码桥接（v6 新增：补"只管设计不管代码"这口气）

设计 Prompt 定稿后，追加本段即可让 AI 输出可运行的前端代码。

## 默认技术栈
单文件 HTML + Tailwind CDN + 原生 JS。零构建，双击即跑，手机浏览器可直接打开。

## 通用代码输出指令（拼在 UI 提示词后面）
```
Now output the above design as a SINGLE self-contained HTML file:
- Tailwind via CDN, custom CSS in <style>, JS at end of <body>
- Mobile-first, max-width 430px centered, 9:19.5 proportions
- All Chinese text must be correct (no garbled characters)
- Images: use CSS gradients / emoji / inline SVG only, NO external image URLs
- All interactive elements must work: tabs switch, buttons respond, popups open/close, selections toggle
- Keep the exact visual style: {风格 token 行}
- No localStorage (static preview only)
```

## 按组件类别的代码要点
- **表单/选择类**（性别选择、筛选、搜索）：选中态切换逻辑 + 下一步按钮可用/禁用态
- **卡片/列表类**（集卡、美食卡）：数据用 JS 数组渲染，方便换内容
- **弹窗类**（底部弹窗、更新弹窗、转盘）：open/close 函数 + 遮罩点击关闭 + 简单入场动画
- **整屏类**（启动页、引导页、个人主页）：分屏结构 + 页面间跳转函数
- **Tab 类**（底部 Tab）：四个页面 div 切换，active 态样式

## 模式 C 项目全案：增加第 6 步"出代码"
逐屏 Prompt 定稿后，对每一屏追加"通用代码输出指令"，得到 N 个单文件 HTML；
再加一个 `index.html` 做目录页，用 iframe 或链接串起所有屏，形成可点击原型。

## 交付物
- `screen-{编号}.html`：单屏可运行文件
- `index.html`：原型目录（仅项目全案）
- 命名中文拼音，注释写中文
