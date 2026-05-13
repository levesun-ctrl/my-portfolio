# 快速参考指南 - 常见编辑任务

## 目录

1. [修改公司信息](#修改公司信息)
2. [修改颜色主题](#修改颜色主题)
3. [添加公司Logo](#添加公司logo)
4. [修改服务和功能](#修改服务和功能)
5. [修改导航菜单](#修改导航菜单)
6. [添加新的部分](#添加新的部分)
7. [修改文本和标题](#修改文本和标题)
8. [联系信息](#联系信息)

---

## 修改公司信息

### 公司名称

找到此行：
```html
<a href="#" class="logo">TechVision</a>
```

替换为你的公司名称：
```html
<a href="#" class="logo">YourCompanyName</a>
```

### 主标题

找到 `<h1>` 标签：
```html
<h1>驱动未来的技术力量</h1>
```

更改为你的标题：
```html
<h1>你的公司主标题</h1>
```

### 副标题

找到 `class="hero-subtitle"` 的段落：
```html
<p class="hero-subtitle">TechVision 为全球企业提供领先的AI、云计算和数据解决方案，助力数字化转型。</p>
```

更改为你的描述：
```html
<p class="hero-subtitle">你的公司描述文本</p>
```

---

## 修改颜色主题

所有颜色定义在 `<style>` 标签中的 `:root` 部分：

```css
:root {
    --primary-dark: #0a0e27;      /* 深色背景 */
    --primary-light: #1a1f3a;     /* 浅色背景 */
    --accent-blue: #00d4ff;       /* 强调蓝色 */
    --accent-purple: #7c3aed;     /* 强调紫色 */
    --text-primary: #ffffff;      /* 主要文本 */
    --text-secondary: #b0b8d4;    /* 次要文本 */
    --border-color: #2d3448;      /* 边框颜色 */
    --bg-hover: #252d47;          /* 悬停背景 */
}
```

### 快速主题

#### 现代企业蓝色
```css
:root {
    --primary-dark: #0f1a3a;
    --primary-light: #1a2d52;
    --accent-blue: #1e90ff;
    --accent-purple: #4169e1;
    --text-primary: #ffffff;
    --text-secondary: #b0c4de;
}
```

#### 绿色生态主题
```css
:root {
    --primary-dark: #0d3622;
    --primary-light: #1a4d2e;
    --accent-blue: #2ecc71;
    --accent-purple: #27ae60;
    --text-primary: #ffffff;
    --text-secondary: #d0d0d0;
}
```

#### 现代红色
```css
:root {
    --primary-dark: #2a0a0a;
    --primary-light: #3d1515;
    --accent-blue: #ff6b6b;
    --accent-purple: #ee5a52;
    --text-primary: #ffffff;
    --text-secondary: #e0e0e0;
}
```

#### 金色奢侈
```css
:root {
    --primary-dark: #1a1410;
    --primary-light: #2a2015;
    --accent-blue: #d4af37;
    --accent-purple: #ffd700;
    --text-primary: #ffffff;
    --text-secondary: #c0c0c0;
}
```

---

## 添加公司Logo

### 方式1：使用文本Logo（推荐）

保留当前代码不变，只修改文本。

### 方式2：添加图片Logo

替换这一行：
```html
<a href="#" class="logo">TechVision</a>
```

改为：
```html
<a href="#" class="logo">
    <img src="path/to/your/logo.png" alt="Company Logo" style="height: 40px;">
</a>
```

确保：
- 将 `path/to/your/logo.png` 替换为你的Logo文件路径
- Logo文件应该放在网站目录中

### 上传Logo文件

1. 在项目根目录创建 `images` 文件夹
2. 上传你的Logo到 `images/logo.png`
3. 更改路径为 `images/logo.png`

---

## 修改服务和功能

### 修改功能卡片

找到 `<!-- Features Section -->` 部分：

```html
<div class="feature-card">
    <div class="feature-icon">🚀</div>
    <h3>快速部署</h3>
    <p>我们的解决方案可以快速集成到您的现有系统中，平均部署时间仅需2周。</p>
</div>
```

修改为：
```html
<div class="feature-card">
    <div class="feature-icon">✨</div>
    <h3>你的功能标题</h3>
    <p>你的功能描述</p>
</div>
```

**Emoji选择提示：**
- 🚀 速度/启动
- 🛡️ 安全
- 📊 数据/分析
- 💡 创意/创新
- 👥 团队/社交
- 🌍 全球/覆盖
- 💰 价格/成本
- ⚡ 性能/速度
- 🎯 目标/精准
- 🔧 工具/配置

### 修改服务项

找到 `<!-- Services Section -->` 部分：

```html
<div class="service-item">
    <div class="service-number">01</div>
    <h3>AI解决方案</h3>
    <p>提供端到端的人工智能应用开发...</p>
    <a href="#" class="service-link">了解更多 →</a>
</div>
```

修改为：
```html
<div class="service-item">
    <div class="service-number">01</div>
    <h3>你的服务名称</h3>
    <p>你的服务描述</p>
    <a href="service-page.html" class="service-link">了解更多 →</a>
</div>
```

---

## 修改导航菜单

找到导航菜单：

```html
<ul id="navMenu">
    <li><a href="#features">功能特性</a></li>
    <li><a href="#services">我们的服务</a></li>
    <li><a href="#testimonials">客户评价</a></li>
    <li><a href="#contact" class="btn-contact">联系我们</a></li>
</ul>
```

### 添加新菜单项

```html
<ul id="navMenu">
    <li><a href="#features">功能特性</a></li>
    <li><a href="#services">我们的服务</a></li>
    <li><a href="about.html">关于我们</a></li>  <!-- 新增 -->
    <li><a href="blog.html">博客</a></li>         <!-- 新增 -->
    <li><a href="#testimonials">客户评价</a></li>
    <li><a href="#contact" class="btn-contact">联系我们</a></li>
</ul>
```

### 删除菜单项

简单地删除对应的 `<li>` 行。

---

## 添加新的部分

### 添加新区域模板

在适当的位置添加以下代码：

```html
<!-- 新部分 -->
<section class="features" id="newsection">
    <div class="container">
        <h2 class="section-title">新部分标题</h2>
        <p class="section-subtitle">副标题说明</p>
        <!-- 在这里添加内容 -->
    </div>
</section>
```

### 更新页脚链接

找到页脚部分：

```html
<div class="footer-section">
    <h3>产品</h3>
    <ul>
        <li><a href="#">AI解决方案</a></li>
        <li><a href="#">云计算平台</a></li>
        <li><a href="#">数据分析</a></li>
        <li><a href="#">系统集成</a></li>
    </ul>
</div>
```

替换为你的内容。

---

## 修改文本和标题

### 主英雄区

```html
<h1>驱动未来的技术力量</h1>
<p class="hero-subtitle">TechVision 为全球企业提供...</p>
```

### 各部分标题

```html
<h2 class="section-title">核心优势</h2>
<p class="section-subtitle">我们拥有业界领先的技术团队和丰富的项目经验</p>
```

### CTA区域

```html
<h2>准备好开始您的数字化之旅了吗？</h2>
<p>联系我们的团队，了解我们如何帮助您的企业实现技术升级和业务增长。</p>
```

---

## 联系信息

### 修改电话

找到：
```html
<li><a href="tel:+8610-1234-5678">电话: +86 10-1234-5678</a></li>
```

改为：
```html
<li><a href="tel:+861012345678">电话: +86 10-1234-5678</a></li>
```

### 修改邮箱

找到：
```html
<li><a href="mailto:info@techvision.com">邮箱: info@techvision.com</a></li>
```

改为：
```html
<li><a href="mailto:your-email@yourdomain.com">邮箱: your-email@yourdomain.com</a></li>
```

### 修改地址

找到：
```html
<li>地址: 北京市朝阳区XX街道</li>
```

改为：
```html
<li>地址: 你的完整地址</li>
```

---

## 修改统计数据

找到 `<!-- Stats Section -->` 部分：

```html
<div class="stat">
    <div class="stat-number">500+</div>
    <div class="stat-label">已服务客户</div>
</div>
```

修改数字和标签为你的实际数据。

---

## 修改客户评价

找到 `<!-- Testimonials Section -->` 部分：

```html
<div class="testimonial">
    <p class="testimonial-text">"TechVision 的AI解决方案..."</p>
    <div class="testimonial-author">
        <div class="author-avatar">李</div>
        <div class="author-info">
            <h4>李明</h4>
            <p>科技公司 CTO</p>
        </div>
    </div>
</div>
```

修改为：
- 评价文本
- 客户名字（用于头像简写，通常用2个字母）
- 客户全名
- 客户职位

---

## 修改页脚版权

找到：
```html
<p>&copy; 2024 TechVision. 保留所有权利。</p>
```

改为：
```html
<p>&copy; 2024 Your Company Name. 保留所有权利。</p>
```

---

## 常见编辑错误

### ❌ 错误

```html
<!-- 缺少闭合标签 -->
<h1>标题</h3>

<!-- 引号不匹配 -->
<p class='text">文本</p>

<!-- 特殊字符未转义 -->
<p>价格：¥100元</p>
```

### ✅ 正确

```html
<!-- 正确的标签闭合 -->
<h1>标题</h1>

<!-- 匹配的引号 -->
<p class="text">文本</p>

<!-- HTML实体 -->
<p>价格：&yen;100元</p>
```

---

## 常用HTML实体

| 字符 | 代码 | 含义 |
|------|------|------|
| & | `&amp;` | AND符号 |
| < | `&lt;` | 小于 |
| > | `&gt;` | 大于 |
| " | `&quot;` | 双引号 |
| ' | `&apos;` | 单引号 |
| © | `&copy;` | 版权 |
| ® | `&reg;` | 注册商标 |
| ™ | `&trade;` | 商标 |
| € | `&euro;` | 欧元 |
| ¥ | `&yen;` | 人民币 |
| £ | `&pound;` | 英镑 |
| → | `&rarr;` | 右箭头 |
| ← | `&larr;` | 左箭头 |

---

## 提交更改到GitHub

每次修改后，使用以下命令提交：

```bash
# 查看修改
git status

# 添加文件
git add .

# 提交更改（添加有意义的提交信息）
git commit -m "Update: Modify company info and colors"

# 推送到GitHub
git push origin main
```

---

## 获取帮助

- 查看 `DEPLOYMENT_GUIDE.md` 了解部署步骤
- 查看 `README.md` 了解功能和自定义选项
- 访问 [HTML教程](https://www.w3schools.com/html/)
- 访问 [CSS教程](https://www.w3schools.com/css/)

祝贺你完成了网站的自定义！🎉
