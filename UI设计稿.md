# BRClient 用户界面设计文档

## 文档信息
- **项目名称**: BRClient
- **文档版本**: v1.0
- **编制日期**: 2025年12月
- **编制人**: UI设计团队
- **基于文档**: 原型图 v1.0

---

## 1. 设计系统规范

### 1.1 设计理念
**核心价值观**:
- **专注**: 专注于AI对话体验，去除多余干扰
- **简洁**: 简洁的视觉语言，清晰的信息层级
- **高效**: 优化交互流程，提升使用效率
- **现代**: 现代化的设计风格，符合当代审美

**设计目标**:
1. 打造专业、可信的品牌形象
2. 提供舒适、流畅的使用体验
3. 确保清晰、易读的信息呈现
4. 支持个性化和可扩展性

### 1.2 品牌识别

#### 1.2.1 品牌色彩
**主色调（AWS风格）**:
- Primary: #FF9900（AWS橙色）- 强调、主要操作
- Secondary: #232F3E（AWS深蓝）- 标题、重要信息
- Accent: #00A9CE（Bedrock蓝）- 辅助、提示

**功能色彩**:
- Success: #28a745（成功状态）
- Warning: #ffc107（警告提示）
- Error: #dc3545（错误状态）
- Info: #17a2b8（信息提示）

#### 1.2.2 Logo设计
**主Logo**:
- 图形：AWS Bedrock图标简化版
- 文字：BRClient（SF Pro Display字体）
- 尺寸：32x32px（应用图标）
- 变体：横版、竖版、纯图标

**应用场景**:
- 应用图标：512x512px PNG
- 启动页：256x256px PNG
- 标题栏：32x32px PNG
- Favicon：16x16px ICO

---

## 2. 视觉风格指南

### 2.1 设计风格定位

#### 2.1.1 风格关键词
- **现代化**: 扁平化设计、微阴影、圆角
- **专业性**: 严谨的栅格、统一的间距
- **科技感**: 渐变色彩、动效过渡
- **人性化**: 温和的色彩、舒适的阅读

#### 2.1.2 视觉层次
1. **第一层级**: 品牌色、大标题、主要按钮
2. **第二层级**: 中性色、小标题、次要按钮
3. **第三层级**: 辅助色、说明文字、图标
4. **背景层级**: 浅色背景、分割线、容器

### 2.2 光影系统

#### 2.2.1 阴影规范
**层级阴影**:
```
Level 1 (悬浮): 
box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

Level 2 (卡片): 
box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);

Level 3 (模态): 
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);

Level 4 (弹出): 
box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
```

#### 2.2.2 渐变规范
**主题渐变**:
- Header渐变: linear-gradient(135deg, #667eea 0%, #764ba2 100%)
- Button渐变: linear-gradient(135deg, #FF9900 0%, #FFB84D 100%)
- 背景渐变: linear-gradient(180deg, #FFFFFF 0%, #F8F9FA 100%)

### 2.3 动效规范

#### 2.3.1 缓动函数
```css
/* 标准缓动 */
ease-standard: cubic-bezier(0.4, 0.0, 0.2, 1);

/* 减速缓动 */
ease-decelerate: cubic-bezier(0.0, 0.0, 0.2, 1);

/* 加速缓动 */
ease-accelerate: cubic-bezier(0.4, 0.0, 1, 1);

/* 弹性缓动 */
ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);
```

#### 2.3.2 动画时长
- **微交互**: 100ms（图标变化）
- **快速**: 200ms（悬停、点击）
- **标准**: 300ms（展开、折叠）
- **缓慢**: 500ms（页面过渡）
- **特殊**: 800ms（启动动画）

#### 2.3.3 动画类型
1. **淡入淡出**: 透明度变化
2. **滑动**: 位置变化
3. **缩放**: 大小变化
4. **旋转**: 角度变化
5. **弹性**: 弹性效果

---

## 3. 色彩方案

### 3.1 亮色主题（Light Theme）

#### 3.1.1 主色板
```
主背景色（Background）:
- bg-primary: #FFFFFF
- bg-secondary: #F8F9FA
- bg-tertiary: #E9ECEF

文字色彩（Text）:
- text-primary: #212529    （主要文字）
- text-secondary: #6C757D  （次要文字）
- text-tertiary: #ADB5BD   （辅助文字）
- text-disabled: #DEE2E6   （禁用文字）

边框色彩（Border）:
- border-primary: #DEE2E6
- border-secondary: #E9ECEF
- border-hover: #CED4DA
```

#### 3.1.2 功能色板
```
品牌色（Brand）:
- brand-primary: #FF9900
- brand-primary-hover: #FFB84D
- brand-primary-active: #E68A00
- brand-primary-light: #FFF3E0

信息色（Semantic）:
- success: #28a745
- success-light: #D4EDDA
- warning: #ffc107
- warning-light: #FFF3CD
- error: #dc3545
- error-light: #F8D7DA
- info: #17a2b8
- info-light: #D1ECF1
```

#### 3.1.3 对话气泡色彩
```
用户消息（User）:
- background: #E3F2FD
- text: #212529
- border: #BBDEFB

AI消息（Assistant）:
- background: #FFFFFF
- text: #212529
- border: #E9ECEF
- accent: #FF9900

系统消息（System）:
- background: #F8F9FA
- text: #6C757D
- border: #DEE2E6
```

### 3.2 暗色主题（Dark Theme）

#### 3.2.1 主色板
```
主背景色（Background）:
- bg-primary: #1E1E1E
- bg-secondary: #252526
- bg-tertiary: #2D2D30

文字色彩（Text）:
- text-primary: #E8E8E8    （主要文字）
- text-secondary: #A0A0A0  （次要文字）
- text-tertiary: #707070   （辅助文字）
- text-disabled: #505050   （禁用文字）

边框色彩（Border）:
- border-primary: #3E3E42
- border-secondary: #2D2D30
- border-hover: #505050
```

#### 3.2.2 功能色板
```
品牌色（Brand）:
- brand-primary: #FFB84D
- brand-primary-hover: #FFC266
- brand-primary-active: #FF9900
- brand-primary-light: #3D2E1F

信息色（Semantic）:
- success: #4CAF50
- success-light: #1B3A1E
- warning: #FFD54F
- warning-light: #3D351F
- error: #F44336
- error-light: #3D1E1B
- info: #29B6F6
- info-light: #1B2F3D
```

#### 3.2.3 对话气泡色彩
```
用户消息（User）:
- background: #1E3A5F
- text: #E8E8E8
- border: #2A5082

AI消息（Assistant）:
- background: #252526
- text: #E8E8E8
- border: #3E3E42
- accent: #FFB84D

系统消息（System）:
- background: #2D2D30
- text: #A0A0A0
- border: #3E3E42
```

### 3.3 色彩使用规则

#### 3.3.1 对比度要求
- 大文字（18px+）: 最小对比度 3:1
- 小文字（<18px）: 最小对比度 4.5:1
- 图标和UI元素: 最小对比度 3:1
- 重要操作按钮: 最小对比度 4.5:1

#### 3.3.2 色彩层级
1. **强调**: 品牌主色，吸引注意
2. **常规**: 中性色，日常使用
3. **辅助**: 浅色，次要信息
4. **背景**: 极浅色，内容承载

---

## 4. 字体排版规范

### 4.1 字体家族

#### 4.1.1 西文字体
```
主字体（Primary Font）:
- 名称: SF Pro Display / SF Pro Text
- 用途: 界面文字、标题
- 备选: -apple-system, BlinkMacSystemFont, "Segoe UI"

代码字体（Monospace Font）:
- 名称: JetBrains Mono / Fira Code
- 用途: 代码块、等宽内容
- 备选: "Courier New", monospace
```

#### 4.1.2 中文字体
```
主字体（Primary Font）:
- 名称: PingFang SC / Microsoft YaHei
- 用途: 中文界面
- 备选: "Helvetica Neue", Arial

数字字体（Numeric Font）:
- 名称: SF Pro Display
- 用途: 数字显示、统计
- 特性: 等宽数字
```

### 4.2 字体大小规范

#### 4.2.1 字号系统
```
特大标题（Hero）: 32px / 2rem
大标题（H1）: 24px / 1.5rem
中标题（H2）: 20px / 1.25rem
小标题（H3）: 18px / 1.125rem
正文（Body）: 16px / 1rem
小字（Small）: 14px / 0.875rem
辅助（Caption）: 12px / 0.75rem
```

#### 4.2.2 行高规范
```
标题行高: 1.2 - 1.3
正文行高: 1.5 - 1.6
代码行高: 1.6 - 1.8
列表行高: 1.4 - 1.5
```

#### 4.2.3 字重规范
```
Thin: 100 (极少使用)
Light: 300 (次要文字)
Regular: 400 (常规文字)
Medium: 500 (强调文字)
Semibold: 600 (小标题)
Bold: 700 (大标题)
```

### 4.3 文字样式定义

#### 4.3.1 标题样式
```
H1 - 页面主标题:
font-size: 24px
font-weight: 600
line-height: 1.3
color: text-primary
margin-bottom: 16px

H2 - 区块标题:
font-size: 20px
font-weight: 600
line-height: 1.3
color: text-primary
margin-bottom: 12px

H3 - 小节标题:
font-size: 18px
font-weight: 500
line-height: 1.3
color: text-primary
margin-bottom: 8px
```

#### 4.3.2 正文样式
```
Body1 - 主要正文:
font-size: 16px
font-weight: 400
line-height: 1.6
color: text-primary

Body2 - 次要正文:
font-size: 14px
font-weight: 400
line-height: 1.5
color: text-secondary

Caption - 辅助文字:
font-size: 12px
font-weight: 400
line-height: 1.4
color: text-tertiary
```

---

## 5. 组件库设计

### 5.1 按钮组件（Button）

#### 5.1.1 主要按钮（Primary Button）
```
默认状态:
- background: brand-primary (#FF9900)
- color: #FFFFFF
- border: none
- border-radius: 4px
- padding: 10px 20px
- font-size: 14px
- font-weight: 500
- box-shadow: Level 1

悬停状态:
- background: brand-primary-hover (#FFB84D)
- box-shadow: Level 2
- transform: translateY(-1px)

按下状态:
- background: brand-primary-active (#E68A00)
- box-shadow: none
- transform: translateY(0px)

禁用状态:
- background: #DEE2E6
- color: #ADB5BD
- cursor: not-allowed
```

#### 5.1.2 次要按钮（Secondary Button）
```
默认状态:
- background: transparent
- color: brand-primary
- border: 1px solid brand-primary
- border-radius: 4px
- padding: 9px 19px

悬停状态:
- background: brand-primary-light
- border-color: brand-primary-hover

按下状态:
- background: brand-primary-light
- border-color: brand-primary-active
```

#### 5.1.3 文字按钮（Text Button）
```
默认状态:
- background: transparent
- color: brand-primary
- border: none
- padding: 8px 16px

悬停状态:
- background: brand-primary-light
- color: brand-primary-hover
```

#### 5.1.4 图标按钮（Icon Button）
```
尺寸: 32x32px
图标: 20x20px
圆角: 4px

默认状态:
- background: transparent
- color: text-secondary

悬停状态:
- background: bg-secondary
- color: text-primary
```

### 5.2 输入框组件（Input）

#### 5.2.1 文本输入框
```
默认状态:
- height: 40px
- padding: 8px 12px
- border: 1px solid border-primary
- border-radius: 4px
- font-size: 14px
- background: bg-primary

聚焦状态:
- border-color: brand-primary
- box-shadow: 0 0 0 3px brand-primary-light

错误状态:
- border-color: error
- box-shadow: 0 0 0 3px error-light

禁用状态:
- background: bg-tertiary
- color: text-disabled
- cursor: not-allowed
```

#### 5.2.2 多行文本框
```
最小高度: 120px (3行)
最大高度: 400px (10行)
padding: 12px
resize: vertical
其他属性: 同文本输入框
```

#### 5.2.3 搜索框
```
前置图标: 🔍 (16x16px)
padding-left: 36px
其他属性: 同文本输入框

快捷键提示:
- position: absolute
- right: 12px
- color: text-tertiary
- font-size: 12px
- content: "⌘K" or "Ctrl+K"
```

### 5.3 对话气泡组件（Message Bubble）

#### 5.3.1 用户消息气泡
```
布局:
- align: right
- max-width: 70%
- margin-left: auto

样式:
- background: 用户消息背景色
- border-radius: 12px 12px 4px 12px
- padding: 12px 16px
- box-shadow: Level 1

内容:
- font-size: 16px
- line-height: 1.6
- color: text-primary
```

#### 5.3.2 AI消息气泡
```
布局:
- align: left
- max-width: 70%
- margin-right: auto

样式:
- background: AI消息背景色
- border: 1px solid border-primary
- border-radius: 12px 12px 12px 4px
- padding: 12px 16px

头部:
- icon: 🤖 (24x24px)
- model: "Claude3 Sonnet" (12px, text-tertiary)
- time: "10:23" (12px, text-tertiary)

操作栏:
- position: absolute top-right
- buttons: 复制 | 重新生成 | 删除
- opacity: 0 (hover时显示)
```

#### 5.3.3 代码块样式
```
容器:
- background: #F6F8FA (light) / #2D2D30 (dark)
- border-radius: 6px
- padding: 16px
- margin: 8px 0
- overflow-x: auto

头部:
- language: (12px, text-tertiary)
- copy-button: (top-right, 32x32px)

代码:
- font-family: JetBrains Mono
- font-size: 14px
- line-height: 1.6
- syntax-highlight: GitHub style
```

### 5.4 列表组件（List）

#### 5.4.1 对话列表项
```
尺寸:
- height: 64px
- padding: 12px 16px

布局:
- icon: 左侧 (32x32px)
- content: 中间 (flex: 1)
  - title: (14px, font-weight: 500)
  - preview: (12px, text-tertiary, 1行省略)
  - time: (12px, text-tertiary)
- actions: 右侧 (hover显示)

状态:
默认:
- background: transparent
- border-bottom: 1px solid border-secondary

悬停:
- background: bg-secondary

选中:
- background: brand-primary-light
- border-left: 3px solid brand-primary
```

#### 5.4.2 设置列表项
```
尺寸:
- height: 48px
- padding: 12px 16px

布局:
- label: 左侧 (14px)
- control: 右侧 (开关/输入框/下拉)

分组:
- group-title: (12px, text-tertiary, padding: 8px 16px)
- separator: (1px solid border-secondary)
```

### 5.5 模态框组件（Modal）

#### 5.5.1 对话框
```
遮罩层:
- background: rgba(0, 0, 0, 0.5)
- backdrop-filter: blur(4px)

容器:
- max-width: 600px
- min-width: 400px
- background: bg-primary
- border-radius: 8px
- box-shadow: Level 4
- padding: 24px

头部:
- height: 48px
- title: (20px, font-weight: 600)
- close-button: (右上角, 32x32px)

内容区:
- padding: 16px 0
- max-height: 60vh
- overflow-y: auto

底部:
- height: 56px
- buttons: 右对齐
- gap: 8px
```

---

## 6. 页面设计说明

### 6.1 主对话页面设计

#### 6.1.1 整体布局
- 左侧边栏（230-500px可调）
- 主内容区（自适应）
- 底部输入区（150-400px可变）

#### 6.1.2 顶部标题栏
```
高度: 60px
背景: bg-primary
边框: 1px solid border-secondary

左侧:
- App Icon (32x32px)
- App Name "BRClient" (16px, font-weight: 600)

右侧:
- 窗口控制按钮 (最小化/最大化/关闭)
- macOS: 左上角三个圆点
- Windows: 右上角三个图标
```

#### 6.1.3 侧边栏设计
```
背景: bg-secondary
边框: 1px solid border-primary (右侧)

顶部区域 (64px):
- 新建对话按钮 (primary, full-width)

搜索区域 (48px):
- 搜索输入框 (带图标和快捷键提示)

对话列表:
- 分组显示: 今天/昨天/本周/更早
- 虚拟滚动优化长列表
- 加载动画: skeleton screen

底部区域 (96px):
- 设置按钮
- 帮助按钮
- 用户信息（可选）
```

#### 6.1.4 对话内容区
```
背景: bg-primary
padding: 24px

消息列表:
- 自动滚动到最新消息
- 虚拟滚动优化性能
- 日期分隔线

消息间距:
- 同用户连续消息: 4px
- 不同用户消息: 16px
- 日期分隔: 24px

空状态:
- icon: 欢迎图标 (96x96px)
- title: "开始新对话" (20px)
- description: 快速入门提示
- examples: 示例问题卡片
```

#### 6.1.5 输入区设计
```
背景: bg-primary
边框: 1px solid border-primary (顶部)
padding: 16px

顶部工具栏:
- 模型选择器 (dropdown)
- Token计数器 (实时更新)

输入框:
- 多行文本框
- placeholder: "输入消息...（支持Markdown）"
- 最小高度: 120px
- 自动扩展: 最大400px

底部工具栏:
- 左侧: 附件按钮（未来功能）
- 右侧: 发送按钮 (primary, 48px宽)

快捷提示:
- "Ctrl+Enter 发送" (12px, text-tertiary)
```

### 6.2 设置页面设计

#### 6.2.1 布局结构
```
全屏模态框:
- width: 80vw (最大1200px)
- height: 80vh
- center: 居中显示

左侧菜单 (200px):
- 设置分类列表
- 图标 + 文字
- 选中状态高亮

右侧内容区:
- padding: 32px
- 滚动区域
```

#### 6.2.2 AWS配置页
```
标题区:
- "AWS Bedrock 访问配置"
- description: 说明文字

表单区:
- Input: Access Key ID
  - label: "Access Key ID *"
  - helper: "在AWS IAM中获取访问密钥"
  
- Input: Secret Access Key
  - label: "Secret Access Key *"
  - type: password
  - toggle: 显示/隐藏按钮
  
- Select: AWS Region
  - label: "AWS Region *"
  - options: 支持Bedrock的区域列表
  - helper: 常用区域说明

测试区:
- 测试连接按钮 (secondary)
- 结果显示:
  - ✅ 成功: 绿色背景 + 延迟/模型数
  - ❌ 失败: 红色背景 + 错误信息

操作区:
- 取消按钮 (text)
- 保存按钮 (primary)
```

#### 6.2.3 界面设置页
```
主题选择:
- 单选按钮组: 亮色/暗色/自动
- 预览卡片: 显示效果示例

语言选择:
- 下拉框: 支持的语言列表
- 说明: "需要重启应用生效"

字体大小:
- 滑块: 12px - 20px
- 实时预览文本

快捷键:
- 表格展示: 功能 | 快捷键
- 可自定义（未来功能）
```

### 6.3 欢迎引导页设计

#### 6.3.1 多步骤引导
```
步骤指示器:
- 进度点: ⚫ ⚪ ⚪
- 当前步骤: 品牌色填充
- 已完成步骤: 勾选图标

步骤1: 欢迎
- Hero image: 产品插图
- 标题: "欢迎使用 BRClient"
- 描述: 产品简介
- 按钮: "开始配置"

步骤2: AWS配置
- 表单: 同设置页AWS配置
- 说明: 配置指引
- 按钮: "跳过" | "测试并继续"

步骤3: 完成
- Success image: 庆祝插图
- 标题: "配置完成"
- 描述: 使用建议
- 按钮: "开始使用"
```

---

## 7. 响应式设计方案

### 7.1 断点定义
```
- xs: < 800px (不支持)
- sm: 800px - 1024px
- md: 1025px - 1440px
- lg: 1441px - 1920px
- xl: > 1920px
```

### 7.2 布局适配

#### 7.2.1 小屏适配 (800-1024px)
- 侧边栏: 固定230px宽度
- 对话气泡: 最大宽度80%
- 字体大小: 保持不变
- 间距: 适当减小

#### 7.2.2 中屏适配 (1025-1440px)
- 侧边栏: 默认300px，可调
- 对话气泡: 最大宽度70%
- 字体大小: 标准尺寸
- 间距: 标准间距

#### 7.2.3 大屏适配 (>1440px)
- 侧边栏: 可扩展至500px
- 对话气泡: 最大宽度60%
- 内容区: 最大宽度1200px，居中
- 字体大小: 可选择放大

### 7.3 高DPI适配
- 使用SVG图标
- 提供@2x, @3x位图资源
- 矢量Logo和插图
- 像素完美对齐

---

## 8. 设计注释规范

### 8.1 尺寸标注
- 使用红色线条标注
- 标注单位: px
- 关键尺寸: 宽度、高度、间距
- 圆角半径单独标注

### 8.2 颜色标注
- 标注格式: #RRGGBB / rgba()
- 包含透明度说明
- 渐变起止颜色
- 阴影颜色和参数

### 8.3 文字标注
- 字体名称
- 字号 / 行高
- 字重
- 颜色
- 对齐方式

### 8.4 交互标注
- 状态说明: 默认/悬停/按下/禁用
- 动画效果: 类型、时长、缓动
- 触发条件: 点击/悬停/聚焦
- 跳转链接: 页面/弹窗

### 8.5 特殊说明
- 组件复用标注
- 响应式行为
- 数据动态加载
- 权限控制逻辑

---

## 9. 设计交付清单

### 9.1 设计稿文件
- [ ] Figma源文件（主设计稿）
- [ ] Sketch文件（备选）
- [ ] 设计规范文档（本文档）
- [ ] 组件库文件

### 9.2 切图资源
- [ ] 应用图标（多尺寸）
- [ ] Logo（多格式）
- [ ] 插图（SVG）
- [ ] 装饰图标（SVG/PNG）

### 9.3 样式代码
- [ ] CSS变量定义
- [ ] 组件样式模板
- [ ] 动画CSS代码
- [ ] 主题切换代码

### 9.4 原型链接
- [ ] 可交互原型链接
- [ ] 演示视频
- [ ] 使用说明文档

### 9.5 设计评审
- [ ] 产品经理审核
- [ ] 开发团队审核
- [ ] 设计团队互评
- [ ] 用户测试反馈

---

## 10. 附录

### 10.1 设计工具
- **主要工具**: Figma
- **辅助工具**: Sketch, Adobe XD
- **原型工具**: Figma, Principle
- **切图工具**: Figma Export, Sketch Export
- **协作工具**: Figma Cloud, Zeplin

### 10.2 设计资源
- **图标库**: Feather Icons, Material Icons
- **插图库**: unDraw, Storyset
- **字体**: Google Fonts, Adobe Fonts
- **配色**: Coolors, Adobe Color

### 10.3 参考资料
- Material Design Guidelines
- Apple Human Interface Guidelines
- Ant Design
- AWS Design System

### 10.4 版本记录
| 版本 | 日期 | 更新内容 | 设计师 |
|------|------|----------|--------|
| v1.0 | 2025-12-21 | 初始设计稿 | UI设计团队 |

### 10.5 审批记录
| 审批人 | 角色 | 审批意见 | 日期 |
|--------|------|----------|------|
| - | 设计总监 | 待审批 | - |
| - | 产品经理 | 待审批 | - |
| - | 前端负责人 | 待审批 | - |

---

**文档结束**
