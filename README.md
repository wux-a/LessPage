# 极简项目主页

一个极简风格的个人项目展示页面，支持一键部署到GitHub Pages。

## 功能特性

- 🎨 极简设计风格
- 📱 响应式布局，支持移动端
- 🔗 项目链接展示
- 🚀 一键部署到GitHub Pages

## 如何使用

### 1. 修改项目链接

编辑 `index.html` 文件，修改项目信息：

```html
<div class="project">
    <h2>项目名称</h2>
    <p>项目描述</p>
    <a href="https://github.com/yourusername/yourproject" target="_blank">查看项目</a>
</div>
```

### 2. 部署到GitHub Pages

#### 方式一：直接部署

1. 将项目推送到GitHub仓库
2. 进入仓库设置 → Pages
3. 选择 `main` 分支和根目录
4. 点击保存，等待部署完成

#### 方式二：使用GitHub Actions（可选）

创建 `.github/workflows/deploy.yml` 文件：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
```

## 自定义样式

编辑 `style.css` 文件可以自定义页面样式：

- 修改颜色主题
- 调整布局结构
- 更改字体大小

## 技术栈

- HTML5
- CSS3
- 纯静态页面，无需依赖

## 浏览器支持

- Chrome (推荐)
- Firefox
- Safari
- Edge

## 许可证

MIT