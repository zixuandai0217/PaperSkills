# 设计规范详细文档

<!-- Why: 论文汇报类演示更适合宽屏投影，同时实际使用中需要亮色和暗色两套主题。 Scope: 为 PPT Generator 增加 16:9 论文默认布局与双主题设计令牌，指导模板和生成结果保持一致。 Verify: 检查本规范明确包含宽屏默认、亮色/暗色主题色板、以及对应的容器与排版规则。 -->

## 布局模式

### 论文汇报默认：16:9 宽屏

- 默认比例：`16:9`
- 适用场景：组会、教室投屏、论文阅读、答辩展示
- 推荐策略：页面铺满浏览器或投屏画面，内容区域按宽屏留白组织

```css
.slide {
  width: 100vw;
  height: 100vh;
  aspect-ratio: 16 / 9;
  padding: 3rem 4.5rem;
}
```

### 可选：9:16 竖屏

- 仅在移动端展示、短视频风格演示、或用户显式要求时启用

## 主题系统

### 暗色主题（默认）

- 背景：`#000000` / `#0a0a0a`
- 主文字：`#ffffff`
- 辅助文字：`#9ca3af`
- 强调色：`#60a5fa` / `#8b5cf6` / `#22d3ee`

```css
body.theme-dark {
  --bg: #0a0a0a;
  --bg-soft: #111827;
  --text: #ffffff;
  --muted: #9ca3af;
  --panel: rgba(255, 255, 255, 0.06);
  --line: rgba(255, 255, 255, 0.08);
}
```

### 亮色主题

- 背景：`#f7f9fc` / `#eef3ff`
- 主文字：`#0f172a`
- 辅助文字：`#475569`
- 强调色：`#2563eb` / `#7c3aed` / `#0891b2`

```css
body.theme-light {
  --bg: #f7f9fc;
  --bg-soft: #eef3ff;
  --text: #0f172a;
  --muted: #475569;
  --panel: rgba(255, 255, 255, 0.72);
  --line: rgba(15, 23, 42, 0.08);
}
```

## 背景效果

### 主背景
- 暗色主题：深色渐变底色
- 亮色主题：浅色渐变底色 + 柔和高光

### 动态光斑（必须包含）
每页必须包含 1~3 个模糊光斑：

```css
.light-spot {
  position: absolute;
  width: 300px;
  height: 300px;
  border-radius: 50%;
  filter: blur(100px);
  opacity: 0.3;
  animation: float 20s ease-in-out infinite;
}

.light-spot-1 { background: #3b82f6; }  /* 蓝色 */
.light-spot-2 { background: #8b5cf6; }  /* 紫色 */
.light-spot-3 { background: #06b6d4; }  /* 青色 */

@keyframes float {
  0%, 100% { transform: translate(0, 0); }
  25% { transform: translate(50px, -30px); }
  50% { transform: translate(-30px, 50px); }
  75% { transform: translate(-50px, -20px); }
}
```

## 字体加载（国内CDN）

```html
<!-- HarmonyOS Sans SC -->
<link href="https://s1.hdslb.com/bfs/static/jinkela/long/font/regular.css" rel="stylesheet">

<!-- 思源黑体备选 -->
<link href="https://fonts.loli.net/css2?family=Noto+Sans+SC:wght@300;400;700;900&display=swap" rel="stylesheet">

<!-- Inter 英文字体 -->
<link href="https://fonts.loli.net/css2?family=Inter:wght@300;400;700;900&display=swap" rel="stylesheet">
```

## 排版层级

```css
/* H1 超大标题 */
.slide-title {
  font-size: 4rem;      /* 64px */
  font-weight: 900;     /* font-black */
  line-height: 1.2;
  color: var(--text);
}

/* H2 副标题 */
.slide-subtitle {
  font-size: 2rem;      /* 32px */
  font-weight: 700;     /* font-bold */
  color: var(--text);
}

/* P 说明文字 */
.slide-text {
  font-size: 1.25rem;   /* 20px */
  font-weight: 300;     /* font-light */
  color: var(--muted);
}
```

## 论文封面信息区

- 论文汇报第一页在主标题下方，默认要有独立的元信息区
- 推荐顺序：
  - `title`
  - `发表时间 · 会议 / 期刊`
  - `作者`
  - `第一作者机构`
- 推荐样式：

```css
.cover-meta {
  display: grid;
  gap: 0.5rem;
  margin-top: 1.25rem;
}

.cover-meta-line {
  font-size: 1.1rem;
  line-height: 1.5;
  color: var(--muted);
}
```

## 间距规范

- 元素间距：space-y-8 以上（32px+）
- 页面内边距：p-8 或 p-12
- 内容居中：flex items-center justify-center

## 页面容器

```css
.slide {
  width: 100vw;
  height: 100vh;
  aspect-ratio: 16/9;
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 3rem 4.5rem;
}
```

## 切换动画

```css
.slide {
  opacity: 0;
  transform: translateX(100%);
  transition: all 0.5s ease-out;
}

.slide.active {
  opacity: 1;
  transform: translateX(0);
}

.slide.prev {
  transform: translateX(-100%);
}
```
