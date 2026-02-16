# DJ KiraKira Portfolio - 完整产品需求文档 (PRD)

**项目名称**: Gloria Pu (DJ KiraKira) 个人作品集网站
**版本**: 1.0
**创建日期**: 2026-02-16
**域名**: https://www.gloriapu.me
**GitHub**: https://github.com/gloriathepenguin/gloria-pu-portfolio
**Vercel**: https://vercel.com/gloriathepenguin/gloria-pu-portfolio

---

## 目录

1. [项目概述](#项目概述)
2. [技术架构](#技术架构)
3. [功能模块](#功能模块)
4. [设计规范](#设计规范)
5. [部署流程](#部署流程)
6. [后续更新流程](#后续更新流程)
7. [维护指南](#维护指南)
8. [故障排除](#故障排除)

---

## 项目概述

### 产品定位
Gloria Pu (DJ KiraKira) 的个人作品集网站，展示其作为 DJ、策展人和艺术家的专业形象和作品。

### 目标用户
- 潜在合作方和活动策划者
- 音乐爱好者和粉丝
- 媒体和行业专业人士

### 核心价值
- 展示专业的 DJ 形象和音乐品味
- 提供演出历史和音乐作品
- 建立个人品牌和联系渠道

### 设计理念
- 简洁优雅的设计美学
- 流畅的滚动动画体验
- 响应式设计，完美适配各种设备
- 以音乐和视觉艺术为核心的内容呈现

---

## 技术架构

### 技术栈

#### 前端
- **HTML5**: 语义化结构
- **CSS3**: 现代样式和动画
  - CSS Custom Properties (变量)
  - CSS Grid & Flexbox 布局
  - CSS Animations & Transitions
  - 响应式设计 (Mobile-first)
- **JavaScript (Vanilla)**:
  - IntersectionObserver API (滚动动画)
  - DOM 操作
  - 事件监听

#### 字体
- **Google Fonts**:
  - Cormorant Garamond (衬线字体)
  - Inter (无衬线字体)

#### 托管与部署
- **Vercel**:
  - 全球 CDN
  - 自动 HTTPS
  - Git 自动部署
  - 边缘网络加速

#### 版本控制
- **Git**: 本地版本管理
- **GitHub**: 远程仓库托管
  - 仓库: gloriathepenguin/gloria-pu-portfolio
  - 分支: main

#### DNS 与域名
- **Cloudflare**: DNS 管理
- **域名**: gloriapu.me
  - 主域名: www.gloriapu.me
  - 重定向: gloriapu.me → www.gloriapu.me

### 文件结构

```
dj-portfolio/
├── index.html              # 主页面
├── images/                 # 图片资源
│   ├── hero-bg.jpeg       # Hero 背景图
│   ├── profile.jpg        # About 头像
│   ├── gallery/           # Gallery 图片集
│   │   ├── IMG_0914.JPG
│   │   ├── IMG_0928.JPG
│   │   └── ...
│   ├── quote-bg-1.jpeg    # Quote 背景装饰
│   ├── quote-bg-2.jpg
│   ├── ...
│   ├── quote-bg-8.jpg
│   ├── listen-back.jpg    # Music 装饰
│   ├── Disco.png          # Disco 球装饰
│   ├── performance-back.jpg # Gigs 背景
│   ├── contact-image.jpg  # Contact 图片
│   └── about-shape-3.png  # About 装饰
├── PRD.md                 # 原始需求文档
├── PRD-COMPLETE.md        # 完整需求文档（本文档）
├── README.md              # 项目说明
└── .gitignore            # Git 忽略配置
```

---

## 功能模块

### 1. Hero Section (英雄区)

**功能**:
- 全屏视觉冲击力的首屏
- 大标题展示 DJ 名称
- 副标题和标语
- 滚动指示器

**技术实现**:
- 背景图片: hero-bg.jpeg
- 自定义音符光标 (SVG)
- 导航栏固定在顶部
- 平滑滚动效果

**内容**:
```
标题: GLORIA PU
副标题: DJ / Curator / Artist
标语: Music as Atmosphere.
导航: About, Gigs, Music, Gallery, Contact
```

---

### 2. Visual Section (视觉展示区)

**功能**:
- 展示 3 张关键视觉图片
- 网格布局
- 滚动时淡入动画

**技术实现**:
- CSS Grid 三列布局
- IntersectionObserver 触发动画
- 响应式：移动端单列

**图片**:
- nature-loves-you.jpeg
- australia.jpeg
- visual-1.jpeg

---

### 3. About Section (关于部分)

**功能**:
- 个人介绍和背景故事
- 专业照片展示
- 装饰图片点缀

**技术实现**:
- 左右双栏布局 (文字 + 图片)
- 段落文字悬停放大效果
- 图片从右侧滑入动画
- 背景装饰图片淡入

**内容**:
```
标题: Gloria Pu (AKA DJ KiraKira)

正文:
- Former investment banker.
  Now building in AI.
  Always moving through sound.

- Raised between Yunnan, Hong Kong, Europe, and Shanghai,
  her sonic language is shaped by movement and contrast.
  African rhythms, tribal textures, and funky grooves meet
  global pop references — refined, rhythmic, and quietly magnetic.

- She brings a sense of structure to the dancefloor —
  precise transitions, controlled tension, effortless flow.

- As a DJ and promoter with SoundsofShanghai, she has played
  at venues including LE Baron and The Nest.
```

**装饰元素**:
- about-shape-3.png (左上方)

---

### 4. Quote Section (引言部分)

**功能**:
- 展示 Jean-Michel Basquiat 名言
- 滚动触发的逐行显示动画
- 背景装饰图片视差效果

**技术实现**:
- Sticky 定位，300vh 高度
- 滚动进度计算
- 文字逐行淡入 + 上移
- 8 张背景图片视差动画

**内容**:
```
第一行: Pay for Soup,
第二行: Build a Fort,
第三行: Set That on Fire.
作者: — Jean-Michel Basquiat
```

**背景装饰** (8 张图片):
- quote-bg-1.jpeg (左上)
- quote-bg-2.jpg (右中上)
- quote-bg-3.jpg (左下)
- quote-bg-4.jpeg (右中)
- quote-bg-5.jpg (右下)
- quote-bg-6.jpg (右上，小图)
- quote-bg-7.jpg (左中，小图)
- quote-bg-8.jpg (右下偏上，小图)

**动画效果**:
- 滚动进度 > 10%: 第一行出现
- 滚动进度 > 30%: 第二行出现，第一行上移
- 滚动进度 > 55%: 第三行出现，前两行继续上移
- 滚动进度 > 80%: 作者名出现
- 背景图片视差移动，透明度变化

---

### 5. Gigs Archive Section (演出档案)

**功能**:
- 展示历史演出记录
- 按年份分组 (2024, 2025)
- 列表项悬停放大效果

**技术实现**:
- 双栏网格布局 (2024 | 2025)
- 年份标题滚动淡入动画
- 列表项 hover scale(1.05)
- 背景图片 (performance-back.jpg)

**内容格式**:
```
[年份]
  [月份] - [场地名称]
```

**2025 年演出**:
- Jan - The Nest X SoundsofShanghai
- Jan - Le Baron X SoundsofShanghai

**2024 年演出**:
- Sept - Le Baron X SoundsofShanghai
- Sept - Charbon Rooftop X SoundsofShanghai
- Sept - The Nest X SoundsofShanghai
- Oct - The Nest X SoundsofShanghai
- Oct - Charbon Rooftop X SoundsofShanghai
- Oct - Nomad X Sounds of Shanghai
- Nov - Nomad X Sounds of Shanghai
- Nov - Pair for two X SoundsofShanghai

---

### 6. Music Section (音乐部分)

**功能**:
- Spotify 播放列表嵌入
- SoundCloud 混音嵌入
- 装饰图片点缀

**技术实现**:
- iframe 嵌入第三方播放器
- 左右装饰图片滚动动画
- 响应式播放器尺寸

**内容**:
- **Spotify Curations**:
  - 嵌入播放列表
  - 标题使用深绿色 (#1F3D2B) + 文字阴影

- **SoundCloud Mixes**:
  - Nu Disco Mix
  - 自定义播放器样式

**装饰元素**:
- listen-back.jpg (左上，旋转 10度)
- Disco.png (右下，旋转 -15度，透明背景)

---

### 7. Gallery Section (图片集)

**功能**:
- 展示 DJ 现场和生活照片
- 瀑布流布局
- 点击放大查看 (Lightbox)

**技术实现**:
- CSS Grid 瀑布流
- 点击触发 Lightbox 模态框
- 左右切换浏览
- ESC 键关闭

**照片列表** (9 张):
1. IMG_0914.JPG
2. IMG_0928.JPG
3. IMG_0979.JPG
4. IMG_1171 2.JPG
5. IMG_4225.JPG
6. P3312763.JPG
7. 闪动7.jpeg
8. 闪动8.jpeg
9. 闪动9.jpeg

---

### 8. Contact Section (联系部分)

**功能**:
- 联系表单
- 邮箱联系方式
- 右侧展示图片

**技术实现**:
- 双栏布局 (表单 + 图片)
- FormSubmit.co 表单服务
- 图片滚动淡入动画

**表单字段**:
- Name (必填)
- Email (必填)
- Message (必填)
- 提交按钮

**邮箱**: pubeigloria@gmail.com

**装饰图片**: contact-image.jpg

---

### 9. Footer (页脚)

**功能**:
- 品牌信息
- 社交媒体链接
- 装饰元素
- 版权信息

**技术实现**:
- 装饰色块滚动动画
- 社交链接 hover 效果
- 深色背景 (#3D2F1F)

**内容**:
```
品牌名: KIRAKIRA
社交链接:
  - LinkedIn: https://www.linkedin.com/in/gloriapu
  - Instagram: https://www.instagram.com/gloria_kirakira
版权: © 2026 Gloria Pu. All rights reserved.
```

---

## 设计规范

### 色彩系统

```css
--ivory: #F6F1E7;           /* 象牙白 - 主背景 */
--ink: #2C2C2C;             /* 墨色 - 主文字 */
--olive: #4a6741;           /* 橄榄绿 - 次要文字 */
--fairway-green: #1f3d2b;   /* 深绿 - 强调色 */
--warm-gray: #D4C5B9;       /* 暖灰 - 分隔线 */
--blush-pink: #D9B2B0;      /* 粉色 - Gallery 背景 */
--sepia-brown: #3D2F1F;     /* 棕褐 - Footer/Gigs 背景 */
```

### 字体系统

```css
--font-display: 'Cormorant Garamond', serif;  /* 标题字体 */
--font-body: 'Inter', sans-serif;              /* 正文字体 */
```

**字号规范**:
- H1: clamp(4rem, 10vw, 8rem)
- H2: clamp(2rem, 5vw, 4rem)
- H3: 1.25rem
- Body: 1.0625rem (17px)
- Small: 0.875rem

### 间距系统

```css
--section-padding: clamp(4rem, 10vh, 8rem);
```

- Section 内边距: 上下 4-8rem，左右 5%
- 内容最大宽度: 1600px
- 网格间距: 2-5rem

### 动画规范

**缓动函数**:
```css
cubic-bezier(0.16, 1, 0.3, 1)  /* 主要动画 */
ease                            /* 简单过渡 */
```

**时长**:
- 快速交互: 0.3s
- 滚动动画: 0.8-1s
- 页面切换: 1.5s

### 响应式断点

```css
@media (max-width: 767px)   /* 移动端 */
@media (max-width: 1024px)  /* 平板 */
```

### 自定义光标

- 全局光标: 音符 SVG (深绿色)
- 交互元素: pointer
- 文本选择: default

---

## 部署流程

### 一、前期准备

#### 1.1 工具安装

确保已安装以下工具:

```bash
# 检查 Git
git --version

# 检查 Node.js 和 npm
node --version
npm --version

# 安装 Vercel CLI
npm install -g vercel

# 安装 GitHub CLI
brew install gh  # macOS
```

#### 1.2 账号注册

- [x] GitHub 账号: gloriathepenguin
- [x] Vercel 账号: 使用 GitHub 登录
- [x] 域名: gloriapu.me (Cloudflare)

---

### 二、本地项目初始化

#### 2.1 创建项目结构

```bash
# 创建项目目录
mkdir dj-portfolio
cd dj-portfolio

# 创建文件结构
mkdir images
mkdir images/gallery
touch index.html
touch README.md
touch .gitignore
```

#### 2.2 添加 .gitignore

```bash
cat > .gitignore << 'EOF'
.DS_Store
node_modules/
.vercel
.env
.env.local
EOF
```

#### 2.3 开发网站

- 编写 HTML、CSS、JavaScript
- 添加图片资源到 images 目录
- 本地测试：直接打开 index.html 或使用 Live Server

---

### 三、Git 版本控制

#### 3.1 初始化 Git 仓库

```bash
cd /Users/pubei/dj-portfolio

# 初始化 Git
git init

# 添加所有文件
git add .

# 创建第一次提交
git commit -m "Initial commit: DJ KiraKira Portfolio Website

- Complete portfolio website for Gloria Pu (DJ KiraKira)
- Includes Hero, About, Quote, Gigs, Music, Gallery, and Contact sections
- Responsive design with scroll animations
- Custom domain ready: gloriapu.me

Co-Authored-By: Claude Sonnet 4.5 <noreply@anthropic.com>"
```

#### 3.2 创建 GitHub 仓库

```bash
# 登录 GitHub CLI
gh auth login

# 创建远程仓库
gh repo create gloria-pu-portfolio --public --source=. --remote=origin

# 配置 Git 缓冲区（避免大文件推送问题）
git config http.postBuffer 524288000

# 推送代码
gh auth setup-git
git push -u origin main
```

**仓库地址**: https://github.com/gloriathepenguin/gloria-pu-portfolio

---

### 四、Vercel 部署

#### 4.1 首次部署

```bash
# 登录 Vercel
vercel login

# 部署项目
cd /Users/pubei/dj-portfolio
vercel

# 回答问题:
# - Set up and deploy? → Yes
# - Which scope? → 选择你的账号
# - Link to existing project? → No
# - What's your project's name? → gloria-pu-portfolio
# - In which directory is your code located? → ./
# - Want to override settings? → No

# 部署到生产环境
vercel --prod
```

**部署后得到**:
- 预览 URL: https://gloria-pu-portfolio.vercel.app
- 项目 Dashboard: https://vercel.com/gloriathepenguin/gloria-pu-portfolio

#### 4.2 连接 GitHub 自动部署

1. 访问 Vercel Dashboard
2. 进入项目 **Settings** → **Git**
3. 点击 **Connect Git Repository**
4. 选择 **GitHub**
5. 选择仓库: **gloria-pu-portfolio**
6. 点击 **Connect**

**结果**: 以后每次 `git push` 都会自动触发 Vercel 部署

---

### 五、域名配置

#### 5.1 在 Vercel 添加域名

1. 进入 Vercel 项目 → **Settings** → **Domains**
2. 点击 **Add Existing**
3. 输入: `gloriapu.me`
4. 勾选: **Redirect gloriapu.me to www.gloriapu.me**
5. 选择: **Connect to an environment** → **Production**
6. 点击 **Save**

#### 5.2 配置 Cloudflare DNS

1. 登录 [dash.cloudflare.com](https://dash.cloudflare.com)
2. 选择域名: **gloriapu.me**
3. 进入 **DNS** → **Records**

**添加记录 1** (www 子域名):
```
Type: CNAME
Name: www
Target: bc5fa1d12dd3ec25.vercel-dns-017.com
Proxy status: DNS only (灰色云)
TTL: Auto
```

**添加记录 2** (根域名):
```
Type: A
Name: @
Value: 76.76.21.21
Proxy status: DNS only (灰色云)
TTL: Auto
```

**或者使用 CNAME** (Cloudflare 支持根域名 CNAME):
```
Type: CNAME
Name: @
Target: bc5fa1d12dd3ec25.vercel-dns-017.com
Proxy status: DNS only (灰色云)
TTL: Auto
```

4. 点击 **Save**

#### 5.3 等待 DNS 生效

- 时间: 5-30 分钟（通常）
- 最长: 24-48 小时

**检查 DNS 状态**:
```bash
# 检查 DNS 解析
dig gloriapu.me
dig www.gloriapu.me

# 或使用在线工具
# https://dnschecker.org/#A/gloriapu.me
```

#### 5.4 验证部署

1. 回到 Vercel **Domains** 页面
2. 点击 **Refresh** 按钮
3. 等待状态变为: **Valid Configuration**
4. Vercel 自动配置 SSL 证书

**最终状态**:
- gloriapu.me → ✅ Valid Configuration
- www.gloriapu.me → ✅ Valid Configuration
- 自动重定向: gloriapu.me → www.gloriapu.me
- HTTPS 已启用

---

### 六、验证和测试

#### 6.1 访问网站

```bash
# HTTP (自动跳转到 HTTPS)
http://gloriapu.me
http://www.gloriapu.me

# HTTPS (最终访问地址)
https://gloriapu.me → 重定向到 → https://www.gloriapu.me
```

#### 6.2 测试功能

- [ ] 所有图片正常加载
- [ ] 滚动动画流畅
- [ ] 导航链接正常跳转
- [ ] Spotify/SoundCloud 播放器正常
- [ ] Gallery Lightbox 正常工作
- [ ] Contact 表单可以提交
- [ ] 移动端响应式正常
- [ ] 所有链接可点击

#### 6.3 性能检查

使用以下工具检查网站性能:
- [PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- Chrome DevTools Lighthouse

---

## 后续更新流程

### 方法一：本地修改 + Git Push（推荐）

这是最专业和便捷的方式，适合所有类型的更新。

#### 步骤 1: 修改文件

```bash
# 进入项目目录
cd /Users/pubei/dj-portfolio

# 使用任何编辑器修改文件
# - VS Code: code .
# - Sublime: subl .
# - Vim: vim index.html
# - 或直接双击文件用文本编辑器打开
```

#### 步骤 2: 查看修改

```bash
# 查看修改了哪些文件
git status

# 查看具体修改内容
git diff
```

#### 步骤 3: 提交修改

```bash
# 添加所有修改的文件
git add .

# 或者只添加特定文件
git add index.html
git add images/new-photo.jpg

# 提交修改（写清楚改了什么）
git commit -m "更新：修改了 About 部分的个人介绍"

# 或者更详细的提交信息
git commit -m "功能：添加新的 Gallery 图片

- 添加了 3 张新的演出照片
- 优化了图片加载性能
- 调整了 Gallery 网格布局"
```

#### 步骤 4: 推送到 GitHub

```bash
# 推送到远程仓库
git push

# 或指定分支（第一次推送时）
git push -u origin main
```

#### 步骤 5: 等待自动部署

- 推送成功后，Vercel 会自动检测到更新
- 30秒-1分钟后，网站自动更新
- 可以在 Vercel Dashboard 查看部署状态

**查看部署状态**:
- 访问: https://vercel.com/gloriathepenguin/gloria-pu-portfolio/deployments
- 或运行: `vercel ls`

---

### 方法二：使用 VS Code（图形界面）

#### 步骤 1: 安装 VS Code

下载地址: [code.visualstudio.com](https://code.visualstudio.com)

#### 步骤 2: 打开项目

```bash
cd /Users/pubei/dj-portfolio
code .
```

#### 步骤 3: 修改文件

- 在 VS Code 左侧文件树中点击文件
- 直接编辑
- 自动保存（可以在设置中启用）

#### 步骤 4: 提交和推送

1. 点击左侧的 **Source Control** 图标（分支图标）
2. 查看修改的文件
3. 在 "Message" 框中输入提交信息
4. 点击 ✓ **Commit** 按钮
5. 点击 **...** 菜单 → **Push**

#### 步骤 5: 等待部署

同上，Vercel 自动部署。

---

### 常见更新场景

#### 场景 1: 更新文字内容

```bash
# 1. 修改 index.html 中的文字
# 2. 提交
git add index.html
git commit -m "更新：修改了 About 部分的个人介绍"
git push
```

#### 场景 2: 添加新图片

```bash
# 1. 将新图片复制到 images 目录
cp ~/Downloads/new-photo.jpg images/

# 2. 在 index.html 中引用新图片
# <img src="images/new-photo.jpg" alt="描述">

# 3. 提交
git add images/new-photo.jpg
git add index.html
git commit -m "功能：添加新的演出照片"
git push
```

#### 场景 3: 更新演出列表

```bash
# 1. 编辑 index.html，在 Gigs 部分添加新演出
# 2. 提交
git add index.html
git commit -m "更新：添加 2026 年 3 月的新演出"
git push
```

#### 场景 4: 修改样式

```bash
# 1. 修改 index.html 中的 <style> 部分
# 2. 提交
git add index.html
git commit -m "样式：调整了 Gallery 的网格间距"
git push
```

#### 场景 5: 替换图片

```bash
# 1. 替换 images 目录中的图片（保持文件名相同）
cp ~/Downloads/new-hero-bg.jpeg images/hero-bg.jpeg

# 2. 提交
git add images/hero-bg.jpeg
git commit -m "更新：替换了 Hero 背景图"
git push
```

---

### Git 常用命令速查

```bash
# 查看状态
git status

# 查看修改内容
git diff

# 添加文件
git add <file>          # 添加指定文件
git add .               # 添加所有修改

# 提交
git commit -m "信息"    # 提交修改

# 推送
git push                # 推送到远程

# 查看历史
git log                 # 查看提交历史
git log --oneline       # 简洁查看

# 撤销修改（危险）
git checkout -- <file>  # 撤销文件修改
git reset HEAD <file>   # 取消暂存

# 查看远程仓库
git remote -v

# 拉取最新代码
git pull
```

---

### 版本回退（紧急恢复）

如果新版本有问题，需要回退到之前的版本：

#### 方法 1: Vercel Dashboard 回滚

1. 访问 Vercel Deployments 页面
2. 找到之前正常的部署版本
3. 点击该版本的 **...** 菜单
4. 选择 **Promote to Production**
5. 确认回滚

#### 方法 2: Git 回退

```bash
# 查看提交历史
git log --oneline

# 回退到指定提交（危险！会丢失之后的修改）
git reset --hard <commit-hash>
git push --force

# 或者创建新提交来撤销（推荐）
git revert <commit-hash>
git push
```

---

## 维护指南

### 日常维护

#### 定期备份

虽然 GitHub 已经是备份，但建议：

```bash
# 定期下载本地副本
cd /Users/pubei
cp -r dj-portfolio dj-portfolio-backup-$(date +%Y%m%d)

# 或创建 Git tag 标记重要版本
git tag -a v1.0 -m "正式上线版本"
git push origin v1.0
```

#### 监控网站

- **定期访问**: https://www.gloriapu.me
- **查看 Vercel Dashboard**: 检查部署状态和访问统计
- **检查邮件**: FormSubmit 会发送表单提交到邮箱

#### 更新依赖

虽然是静态网站，但 Vercel 可能更新：
- 定期查看 Vercel 通知
- 关注 Vercel 的重要更新公告

---

### 性能优化

#### 图片优化

```bash
# 使用 ImageOptim 压缩图片（macOS）
# 或使用在线工具: tinypng.com

# 建议:
# - JPEG 质量: 80-85%
# - PNG: 使用 TinyPNG 压缩
# - 单张图片大小 < 500KB
```

#### 代码优化

- 定期检查和清理未使用的 CSS
- 优化 JavaScript 性能
- 使用 Chrome DevTools 分析性能

---

### 安全维护

#### Git 安全

```bash
# 永远不要提交敏感信息
# .gitignore 已配置忽略:
# - .env 文件
# - API 密钥
# - 个人隐私信息
```

#### 表单安全

- FormSubmit.co 提供基本的垃圾邮件防护
- 定期检查邮箱，清理垃圾提交

#### HTTPS 证书

- Vercel 自动更新 SSL 证书
- 无需手动维护

---

### 域名续费

- Cloudflare 域名需要**每年续费**
- 设置自动续费以避免域名过期
- 提前 1-2 个月收到续费提醒

---

## 故障排除

### 网站无法访问

#### 问题 1: DNS 未生效

**症状**: 访问 gloriapu.me 显示 "无法访问此网站"

**解决**:
```bash
# 检查 DNS
dig gloriapu.me
dig www.gloriapu.me

# 如果返回空或错误 IP，检查 Cloudflare DNS 设置
```

#### 问题 2: SSL 证书问题

**症状**: 浏览器显示 "不安全" 或证书错误

**解决**:
1. 访问 Vercel Domains 页面
2. 点击 Refresh 按钮
3. 等待 SSL 证书重新生成（5-30分钟）

#### 问题 3: 页面显示 404

**症状**: 访问网站显示 "404 Not Found"

**解决**:
1. 检查 Vercel Deployments 是否成功
2. 检查 index.html 是否在根目录
3. 检查域名配置是否正确

---

### 部署失败

#### 问题 1: Git Push 失败

**症状**: `git push` 报错

**解决**:
```bash
# 检查网络连接
ping github.com

# 重新认证
gh auth login

# 增加缓冲区
git config http.postBuffer 524288000

# 重试推送
git push
```

#### 问题 2: Vercel 部署失败

**症状**: Vercel Dashboard 显示部署失败

**解决**:
1. 查看 Vercel 部署日志
2. 检查是否有语法错误
3. 检查文件路径是否正确
4. 重新部署: `vercel --prod --force`

---

### 图片加载问题

#### 问题: 图片显示不出来

**症状**: 网页上图片显示为损坏图标

**解决**:
```bash
# 检查文件是否存在
ls -la images/

# 检查文件名是否正确（大小写敏感）
# 正确: images/hero-bg.jpeg
# 错误: images/Hero-BG.jpeg

# 检查 HTML 中的路径
# 相对路径: images/photo.jpg
# 绝对路径: /images/photo.jpg
```

---

### Git 相关问题

#### 问题 1: 忘记提交就修改了

**解决**:
```bash
# 保存当前修改
git stash

# 切换到之前的状态
git checkout <commit-hash>

# 恢复修改
git stash pop
```

#### 问题 2: 提交了错误的文件

**解决**:
```bash
# 如果还没 push，撤销最后一次提交
git reset HEAD~1

# 如果已经 push，创建新提交来修正
git revert HEAD
git push
```

---

### 联系支持

#### Vercel 支持
- 文档: https://vercel.com/docs
- 社区: https://github.com/vercel/vercel/discussions
- Email: support@vercel.com

#### GitHub 支持
- 文档: https://docs.github.com
- 社区: https://github.community

#### Cloudflare 支持
- 文档: https://developers.cloudflare.com
- 社区: https://community.cloudflare.com

---

## 附录

### A. 完整配置清单

#### Cloudflare DNS 配置

```
Type: CNAME | Name: www | Value: bc5fa1d12dd3ec25.vercel-dns-017.com | Proxy: DNS only
Type: A    | Name: @   | Value: 76.76.21.21 | Proxy: DNS only
```

#### Vercel 项目设置

```
Project Name: gloria-pu-portfolio
Framework: Other
Build Command: (none)
Output Directory: (none)
Install Command: (none)
Root Directory: ./
Node.js Version: (default)
```

#### Git 配置

```bash
git config user.name "Gloria Pu"
git config user.email "pubeigloria@gmail.com"
git config http.postBuffer 524288000
```

---

### B. 快速命令参考

#### 更新网站（最常用）

```bash
cd /Users/pubei/dj-portfolio
# 修改文件...
git add .
git commit -m "更新内容描述"
git push
```

#### 查看部署状态

```bash
# Vercel CLI
vercel ls

# 或访问网页
open https://vercel.com/gloriathepenguin/gloria-pu-portfolio
```

#### 紧急回滚

```bash
# 在 Vercel Dashboard 操作
# 或使用 CLI
vercel rollback
```

---

### C. 资源链接

#### 项目地址
- **网站**: https://www.gloriapu.me
- **GitHub**: https://github.com/gloriathepenguin/gloria-pu-portfolio
- **Vercel**: https://vercel.com/gloriathepenguin/gloria-pu-portfolio

#### 社交媒体
- **LinkedIn**: https://www.linkedin.com/in/gloriapu
- **Instagram**: https://www.instagram.com/gloria_kirakira
- **Email**: pubeigloria@gmail.com

#### 第三方服务
- **表单服务**: FormSubmit.co
- **DNS**: Cloudflare
- **托管**: Vercel
- **代码仓库**: GitHub

---

### D. 版本历史

#### v1.0 - 2026-02-16
- ✅ 初始版本上线
- ✅ 完整的 8 个功能模块
- ✅ 响应式设计
- ✅ 自定义域名配置
- ✅ Git 自动部署
- ✅ HTTPS 启用

---

## 结语

恭喜！Gloria Pu (DJ KiraKira) 的个人作品集网站已经完全上线并运行。

这个网站具备：
- ✅ 专业的视觉设计
- ✅ 流畅的用户体验
- ✅ 完善的技术架构
- ✅ 简便的更新流程
- ✅ 可靠的部署系统

以后只需要简单的 `git push`，就能让全世界看到你的最新更新。

**Keep creating, keep moving through sound.** 🎵

---

**文档维护**:
- 作者: Claude Sonnet 4.5
- 最后更新: 2026-02-16
- 版本: 1.0
