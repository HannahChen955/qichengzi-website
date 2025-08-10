# 七橙子网站 - Vercel 部署指南

## 🚀 快速部署步骤

### 1. 准备 GitHub 仓库（推荐方式）

```bash
# 在项目目录下初始化 Git
git init
git add .
git commit -m "Initial commit: 七橙子官网"

# 推送到 GitHub（创建一个新的私有或公有仓库）
git remote add origin https://github.com/你的用户名/qichengzi-website.git
git branch -M main
git push -u origin main
```

### 2. Vercel 部署

1. 访问 [vercel.com](https://vercel.com)
2. 使用 GitHub 账号登录
3. 点击 "New Project"
4. 导入你的 GitHub 仓库
5. 配置设置：
   - **Framework Preset**: Other
   - **Root Directory**: `./` (根目录)
   - **Build Command**: 留空（静态网站）
   - **Output Directory**: `./` (根目录)
6. 点击 "Deploy"

### 3. 自定义域名配置

部署成功后：

1. 进入项目的 Vercel Dashboard
2. 点击 "Settings" → "Domains"  
3. 添加域名：`7chengzi.cn`
4. 配置 DNS 记录：

**在你的域名提供商处添加以下记录：**

```
类型: A
名称: @
值: 76.76.19.61

类型: CNAME  
名称: www
值: cname.vercel-dns.com
```

### 4. SSL 证书

Vercel 会自动为你的域名提供免费的 SSL 证书。

## 📁 项目文件结构

```
recruitment_rag_system/
├── index.html          # 主页文件
├── images/             # 图片资源
├── vercel.json         # Vercel 配置
├── .vercelignore       # 部署忽略文件
└── VERCEL_DEPLOY.md    # 部署指南
```

## 🔧 本地开发

```bash
# 启动本地服务器预览
python3 -m http.server 3333
# 访问 http://localhost:3333
```

## 📞 部署后验证

部署成功后，访问：
- Vercel 提供的默认域名（如：qichengzi-website.vercel.app）
- 自定义域名：https://7chengzi.cn

确认：
- ✅ Logo 正确显示
- ✅ 所有图片正常加载  
- ✅ 导航链接工作正常
- ✅ 表单功能正常
- ✅ 响应式设计在不同设备上正常

## 🎯 下一步

1. 配置网站分析（如 Google Analytics）
2. 设置表单提交处理（使用 Formspree 或 Netlify Forms）
3. 添加 sitemap.xml 用于 SEO
4. 配置 robots.txt

---

🍊 **七橙子 | 遇见AI，连接未来**