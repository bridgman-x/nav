# 🧭 个人导航主页

基于 [WebStack-Hugo](https://github.com/oulh/nav) 构建的个人导航页面。

## 快速部署（推荐 Cloudflare Pages）

### 第一步：Fork 模板
1. 打开 https://github.com/oulh/nav
2. 点击右上角 **Fork** 按钮，复制到自己的 GitHub 账号

### 第二步：替换配置文件
1. 进入你 Fork 的仓库
2. 删除原有的 `hugo.yaml` 和 `data/webstack.yml`
3. 上传本模板中的两个文件到对应位置
4. 修改 `hugo.yaml` 中的 `baseURL` 为你的域名

### 第三步：绑定 Cloudflare Pages
1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. 进入 **Pages** → **Create a project** → **Connect to Git**
3. 选择你 Fork 的仓库
4. 构建设置：
   - Build command: `hugo --gc --minify`
   - Build output directory: `public`
5. 点击 **Save and Deploy**

### 第四步：绑定个人域名
1. 部署成功后，进入项目设置 → **Custom domains**
2. 添加你的个人域名
3. 按提示在域名 DNS 添加 CNAME 记录
4. 等待 SSL 证书自动颁发（约 1-2 分钟）

## 日常维护

只需修改 `data/webstack.yml` 文件：

```yaml
- title: 网站名称        # 显示名称
  url: https://...      # 跳转链接
  logo: https://...     # 网站图标（可选，留空自动生成）
  description: 描述     # 鼠标悬停显示
```

每次提交修改后，Cloudflare Pages 会自动重新构建部署。

## 自定义样式（可选）

在 `assets/css/custom.css` 中添加自定义 CSS：

```css
/* 修改主色调 */
:root {
  --primary-color: #6366f1;
}

/* 修改卡片圆角 */
.site-card {
  border-radius: 16px;
}
```

## 图标说明

分类图标使用 [Bootstrap Icons](https://icons.getbootstrap.com/)，格式为 `bi bi-xxx`。

常用图标：
- `bi bi-tools` - 工具
- `bi bi-code-slash` - 开发
- `bi bi-book` - 学习
- `bi bi-people` - 社交
- `bi bi-music-note-beamed` - 娱乐
- `bi bi-calendar-check` - 日常
- `bi bi-briefcase` - 工作
- `bi bi-cloud` - 云服务
- `bi bi-credit-card` - 金融
- `bi bi-heart` - 收藏

## 资源

- 主题文档：https://github.com/oulh/nav
- Hugo 文档：https://gohugo.io/documentation/
- 图标库：https://icons.getbootstrap.com/
