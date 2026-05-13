# GitHub Pages 部署指南

本指南将帮助你快速将 TechVision 网站部署到 GitHub Pages。

## 前置要求

- GitHub 账户
- Git 安装在你的电脑上（[下载地址](https://git-scm.com)）
- 基础的命令行知识

## 部署步骤

### 步骤 1: 创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角的 `+` 图标，选择 `New repository`
3. **重要**: 将仓库命名为 `username.github.io`
   - 将 `username` 替换为你的 GitHub 用户名
   - 例如: `john-doe.github.io`
4. 添加描述（可选）
5. 选择 `Public`（公开）
6. 不需要初始化 README
7. 点击 `Create repository`

### 步骤 2: 克隆仓库

打开命令行，执行以下命令：

```bash
# 导航到你想存储项目的目录
cd path/to/your/projects

# 克隆你的仓库
git clone https://github.com/username/username.github.io.git

# 进入项目目录
cd username.github.io
```

### 步骤 3: 添加网站文件

1. 将以下文件复制到项目目录：
   - `index.html` - 主网站文件
   - `README.md` - 项目说明
   - `_config.yml` - Jekyll 配置
   - `.gitignore` - Git 忽略规则

2. 你的目录结构应该是这样的：
```
username.github.io/
├── index.html
├── README.md
├── _config.yml
└── .gitignore
```

### 步骤 4: 配置 Git（首次使用）

如果你第一次使用 Git，需要配置用户信息：

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 步骤 5: 提交并推送文件

```bash
# 添加所有文件
git add .

# 提交更改
git commit -m "Initial commit: Add website"

# 推送到 GitHub
git push origin main
```

### 步骤 6: 验证发布

1. 等待 1-2 分钟
2. 访问 `https://username.github.io`
3. 你应该能看到你的网站

## 使用自定义域名

如果你有自己的域名，可以连接到 GitHub Pages：

### 方式 1: 使用 DNS 记录

1. 在你的域名注册商处，找到 DNS 设置
2. 添加以下 DNS 记录：
   ```
   A 记录: @        -> 185.199.108.153
   A 记录: @        -> 185.199.109.153
   A 记录: @        -> 185.199.110.153
   A 记录: @        -> 185.199.111.153
   ```
3. 或者添加 CNAME 记录：
   ```
   CNAME 记录: www -> username.github.io
   ```

4. 在 GitHub 仓库设置中：
   - 进入 Settings → Pages
   - 在 "Custom domain" 中输入你的域名
   - 启用 "Enforce HTTPS"

### 方式 2: 使用 CNAME 文件（更推荐）

1. 在项目根目录创建 `CNAME` 文件
2. 添加你的域名：
   ```
   yourdomain.com
   ```
3. 提交并推送：
   ```bash
   git add CNAME
   git commit -m "Add custom domain"
   git push origin main
   ```

4. 在你的域名注册商处添加 CNAME 记录指向 `username.github.io`

## 更新网站内容

每当你修改 `index.html` 或其他文件后：

```bash
# 查看有哪些文件被修改
git status

# 添加所有修改
git add .

# 提交更改（添加有意义的提交信息）
git commit -m "Update: Add new features section"

# 推送到 GitHub
git push origin main
```

刷新你的网站，新内容应该会在 1-2 分钟内显示。

## 常见问题

### Q: 网站没有显示
**A:** 
- 检查仓库名称是否正确（必须是 `username.github.io`）
- 确保文件被推送到了 GitHub
- 等待几分钟，GitHub 需要时间构建网站
- 清除浏览器缓存后重试

### Q: 404 错误
**A:**
- 确保 `index.html` 在仓库根目录
- 检查 GitHub Pages 是否已启用
- 访问 Settings → Pages 检查发布状态

### Q: 修改后网站没更新
**A:**
- 确保所有更改都已提交：`git commit -m "message"`
- 确保已推送到 GitHub：`git push origin main`
- 清除浏览器缓存（Ctrl+Shift+Delete）
- 等待 1-2 分钟

### Q: 想使用子目录发布
**A:**
如果仓库不是 `username.github.io`，可以使用 `/docs` 目录发布：

1. 创建 `docs/` 目录
2. 将 `index.html` 放入 `docs/`
3. 在 Settings → Pages 选择 "docs" 作为发布源
4. 网址将是 `https://username.github.io/reponame`

### Q: 如何添加多个页面？
**A:**
创建新的 HTML 文件，例如：
- `about.html` - 关于页面
- `blog.html` - 博客页面
- `contact.html` - 联系页面

然后在 `index.html` 中链接到这些页面。

### Q: 可以添加 HTTPS 吗？
**A:**
是的！GitHub Pages 自动为所有网站提供 HTTPS。

### Q: 如何查看发布日志？
**A:**
1. 进入仓库主页
2. 点击 "Actions" 选项卡
3. 查看部署历史和可能的错误

## 版本控制基础

### 基本命令

```bash
# 查看文件状态
git status

# 查看修改内容
git diff

# 查看提交历史
git log

# 撤销最后一次提交（未推送）
git reset HEAD~1

# 撤销文件修改
git checkout filename
```

## 安全建议

1. **不要提交敏感信息**
   - API 密钥
   - 密码
   - 个人邮箱（如果不想公开）

2. **使用 .gitignore**
   - 自动忽略敏感文件
   - 参考已提供的 `.gitignore` 模板

3. **启用 GitHub 两因素认证**
   - 提高账户安全

## 高级配置

### 自定义 Jekyll 主题

编辑 `_config.yml`：
```yaml
theme: jekyll-theme-minimal
```

可选的主题：
- `jekyll-theme-cayman`
- `jekyll-theme-minimal`
- `jekyll-theme-slate`
- 更多主题查看 [GitHub Pages 官方文档](https://pages.github.com/themes/)

### 添加 Google Analytics

在 `index.html` 的 `</head>` 前添加：
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

## 部署检查清单

在推送到 GitHub 前，检查以下内容：

- [ ] 修改了 `index.html` 中的公司名称
- [ ] 更新了联系信息（电话、邮箱）
- [ ] 修改了页脚中的版权年份
- [ ] 测试了所有链接
- [ ] 检查了移动设备响应式设计
- [ ] 删除或更新了占位符内容
- [ ] 所有图片链接都正确（如有）

## 获取帮助

- [GitHub Pages 官方文档](https://docs.github.com/en/pages)
- [GitHub Pages 疑难排解](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-common-issues-with-github-pages)
- [Git 学习资源](https://git-scm.com/doc)

## 下一步

部署完成后，你可以：

1. **自定义设计**
   - 修改颜色主题
   - 更改字体
   - 调整布局

2. **添加内容**
   - 上传公司 logo
   - 添加产品图片
   - 编写详细的服务描述

3. **扩展功能**
   - 添加博客页面
   - 集成联系表单
   - 添加搜索引擎优化（SEO）

4. **维护网站**
   - 定期更新内容
   - 监控网站统计
   - 收集用户反馈

祝贺你成功部署了你的网站！🎉
