# TechVision 公司网站

一个现代化、响应式的技术公司网站模板，可直接部署到GitHub Pages。

## 功能特性

- ✨ 现代化设计 - 采用最新的设计趋势和交互体验
- 📱 完全响应式 - 完美适配所有设备（桌面、平板、手机）
- ⚡ 快速加载 - 纯HTML/CSS/JavaScript，无依赖
- 🎨 高度可定制 - 轻松修改颜色、文本和内容
- 🔍 SEO友好 - 包含必要的元标签和结构化数据
- 🚀 即用型 - 开箱即用，无需构建过程

## 包含的部分

- **导航栏** - 固定顶部导航，支持移动菜单
- **英雄区** - 吸引人的主视觉和行动号召
- **功能特性** - 展示产品/服务的核心优势
- **服务列表** - 详细的服务或产品展示
- **统计数据** - 关键数字和成就展示
- **客户评价** - 来自真实客户的推荐信
- **行动号召** - 促进用户转化的区域
- **页脚** - 包含重要链接和联系信息

## 快速开始

### 方式1：直接部署到GitHub Pages

1. **创建新仓库**
   - 在GitHub上创建新仓库，命名为 `username.github.io`（将username替换为你的GitHub用户名）

2. **克隆仓库**
   ```bash
   git clone https://github.com/username/username.github.io.git
   cd username.github.io
   ```

3. **上传文件**
   - 将 `index.html` 文件放入仓库根目录

4. **提交并推送**
   ```bash
   git add index.html
   git commit -m "Initial commit: Add website"
   git push origin main
   ```

5. **访问网站**
   - 打开 `https://username.github.io` 查看你的网站

### 方式2：使用现有仓库

如果你已有项目仓库，将 `index.html` 放在 `docs/` 目录：

1. 在仓库设置中启用 GitHub Pages
2. 选择 `docs/` 文件夹作为源
3. 网站将在 `https://username.github.io/reponame` 发布

## 自定义指南

### 修改公司信息

在 `index.html` 中查找并修改以下内容：

```html
<!-- 公司名称 -->
<a href="#" class="logo">YourCompanyName</a>

<!-- 标题和副标题 -->
<h1>你的主标题</h1>
<p class="hero-subtitle">你的副标题</p>

<!-- 联系信息 -->
<li><a href="tel:+8610-1234-5678">电话: +86 10-1234-5678</a></li>
<li><a href="mailto:info@yourcompany.com">邮箱: info@yourcompany.com</a></li>
```

### 修改颜色主题

在 CSS 部分修改 `:root` 变量：

```css
:root {
    --primary-dark: #0a0e27;      /* 主深色 */
    --primary-light: #1a1f3a;     /* 主浅色 */
    --accent-blue: #00d4ff;       /* 强调蓝色 */
    --accent-purple: #7c3aed;     /* 强调紫色 */
    --text-primary: #ffffff;      /* 主文本 */
    --text-secondary: #b0b8d4;    /* 副文本 */
}
```

### 添加你的logo

查找 `<a href="#" class="logo">TechVision</a>` 并修改为：

```html
<a href="#" class="logo">
    <img src="path/to/your/logo.png" alt="Logo" style="height: 40px;">
</a>
```

### 修改功能特性

在 `<!-- Features Section -->` 部分修改卡片内容：

```html
<div class="feature-card">
    <div class="feature-icon">🚀</div>
    <h3>你的功能标题</h3>
    <p>功能描述文本</p>
</div>
```

### 修改服务列表

在 `<!-- Services Section -->` 部分修改服务项：

```html
<div class="service-item">
    <div class="service-number">01</div>
    <h3>服务名称</h3>
    <p>服务描述</p>
    <a href="#" class="service-link">了解更多 →</a>
</div>
```

## 添加更多页面

如果需要添加更多页面（如博客、关于等），创建新的HTML文件：

```bash
# 创建关于页面
about.html

# 创建博客页面  
blog.html
```

然后在导航菜单中添加链接：

```html
<li><a href="about.html">关于我们</a></li>
```

## 高级自定义

### 添加自定义字体

在 `<head>` 中添加Google Fonts：

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700;900&display=swap" rel="stylesheet">
```

然后在CSS中使用：

```css
body {
    font-family: 'Poppins', sans-serif;
}
```

### 添加表单

在CTA部分添加联系表单：

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="email" name="email" required placeholder="您的邮箱">
    <textarea name="message" required placeholder="留言内容"></textarea>
    <button type="submit">提交</button>
</form>
```

### 集成分析

在 `</head>` 前添加Google Analytics：

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_ID');
</script>
```

## 浏览器支持

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

## 性能优化

- 文件大小：< 50KB
- 加载时间：< 1秒
- Lighthouse评分：90+

## 常见问题

**Q: 如何更改域名？**
A: 购买域名后，在GitHub仓库设置中配置自定义域名。

**Q: 可以添加电商功能吗？**
A: 可以，可以集成 Stripe、PayPal 等支付网关。

**Q: 如何添加博客功能？**
A: 可以使用 Jekyll（GitHub Pages 原生支持）或集成外部博客平台。

**Q: 网站支持HTTPS吗？**
A: 是的，GitHub Pages 自动为所有用户启用 HTTPS。

## 许可证

MIT License - 自由使用和修改

## 技术栈

- HTML5
- CSS3 (with CSS Variables)
- JavaScript (Vanilla)
- 无框架依赖

## 贡献

欢迎提交问题和改进建议！

## 支持

如有问题，请联系：info@techvision.com

---

**提示**: 记得修改所有占位符文本和联系信息为你的实际信息！
