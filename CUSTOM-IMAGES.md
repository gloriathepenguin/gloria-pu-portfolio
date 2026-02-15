# 如何使用自定义背景图片

## 🖼️ 方法 1：本地图片（推荐）

### 步骤 1：准备图片
1. 将你的背景图片放到项目文件夹中
2. 建议创建 `images` 文件夹来组织图片

```bash
mkdir /Users/pubei/dj-portfolio/images
# 然后将你的图片复制到这个文件夹
```

### 步骤 2：修改 index.html

打开 `index.html`，找到第 183-190 行的 `.hero::before` 样式，修改为：

```css
.hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image:
        linear-gradient(rgba(246, 241, 231, 0.3), rgba(246, 241, 231, 0.7)),
        url('images/your-image.jpg');  /* 👈 改成你的图片文件名 */
    background-size: cover;
    background-position: center;
    opacity: 0.4;
}
```

### 步骤 3：调整叠加效果（可选）

**调整透明度：**
```css
/* 更透明（看到更多图片） */
linear-gradient(rgba(246, 241, 231, 0.1), rgba(246, 241, 231, 0.5))

/* 更不透明（文字更清晰） */
linear-gradient(rgba(246, 241, 231, 0.5), rgba(246, 241, 231, 0.9))
```

**使用深色叠加：**
```css
linear-gradient(rgba(18, 18, 18, 0.3), rgba(18, 18, 18, 0.7))
/* 注意：深色背景需要将文字改为浅色 */
```

**使用品牌色叠加：**
```css
/* Fairway Green 叠加 */
linear-gradient(rgba(31, 61, 43, 0.3), rgba(31, 61, 43, 0.7))
```

---

## 🌐 方法 2：在线图片 URL

如果你的图片已经上传到图床或 CDN：

```css
.hero::before {
    background-image:
        linear-gradient(rgba(246, 241, 231, 0.3), rgba(246, 241, 231, 0.7)),
        url('https://your-image-host.com/path/to/image.jpg');
    background-size: cover;
    background-position: center;
}
```

### 推荐的免费图床服务：
- **Imgur**: https://imgur.com
- **Cloudinary**: https://cloudinary.com (免费额度)
- **ImgBB**: https://imgbb.com

---

## 📐 图片尺寸建议

- **最小宽度**: 1920px
- **最小高度**: 1080px  
- **推荐比例**: 16:9 或 21:9
- **文件大小**: 建议 < 500KB（优化后）
- **格式**: JPG (照片) 或 PNG (图形)

### 图片优化工具：
- **TinyPNG**: https://tinypng.com
- **Squoosh**: https://squoosh.app
- **ImageOptim**: https://imageoptim.com (Mac)

---

## 🎨 图片风格建议

根据 PRD 的 Editorial + Soft Luxury 定位，建议使用：

✅ **推荐风格：**
- 柔和的自然光线
- 中性色调（米色、灰色、绿色）
- 极简主义构图
- 建筑/空间摄影
- 抽象纹理

❌ **避免：**
- 过于鲜艳的颜色
- 复杂混乱的背景
- 低分辨率图片
- 过度饱和的色彩

---

## 🎭 Pencil 版本使用自定义图片

Pencil 目前只支持通过 URL 使用图片。如果你想在 Pencil 中使用自己的图片：

### 选项 1：先上传到图床，然后使用 URL
```javascript
// 在 Pencil 中使用你的图片 URL
G("zyyV6", "stock", "YOUR_IMAGE_URL")
```

### 选项 2：暂时使用 stock 图片，之后在 HTML 中替换
Pencil 主要用于设计和布局，最终的图片可以在 HTML 版本中替换。

---

## 🔍 测试你的更改

保存 `index.html` 后：

1. **在浏览器中打开**
   ```bash
   open /Users/pubei/dj-portfolio/index.html
   ```

2. **或启动本地服务器**
   ```bash
   cd /Users/pubei/dj-portfolio
   python -m http.server 8000
   # 然后访问 http://localhost:8000
   ```

3. **检查图片是否显示**
   - 按 F12 打开开发者工具
   - 查看 Console 是否有错误
   - 检查 Network 标签确认图片已加载

---

## 💡 故障排除

### 图片不显示？

**检查路径：**
```
✅ 正确: url('images/hero.jpg')
✅ 正确: url('../images/hero.jpg')  
✅ 正确: url('https://example.com/hero.jpg')
❌ 错误: url(images/hero.jpg)  ← 缺少引号
❌ 错误: url('image/hero.jpg')  ← 拼写错误
```

**检查文件是否存在：**
```bash
ls -la /Users/pubei/dj-portfolio/images/
```

**检查文件权限：**
```bash
chmod 644 /Users/pubei/dj-portfolio/images/your-image.jpg
```

### 图片显示但模糊？

- 使用更高分辨率的图片（至少 1920px 宽）
- 确保 `background-size: cover` 已设置
- 优化图片质量（不要过度压缩）

### 文字看不清？

调整叠加层透明度或颜色：
```css
/* 增加叠加层不透明度 */
linear-gradient(rgba(246, 241, 231, 0.6), rgba(246, 241, 231, 0.9))
```

---

## 📝 示例配置

### 示例 1：使用本地图片
```css
background-image:
    linear-gradient(rgba(246, 241, 231, 0.4), rgba(246, 241, 231, 0.8)),
    url('images/studio-background.jpg');
```

### 示例 2：使用在线图片
```css
background-image:
    linear-gradient(rgba(246, 241, 231, 0.3), rgba(246, 241, 231, 0.7)),
    url('https://images.unsplash.com/photo-1234567890');
```

### 示例 3：深色氛围
```css
background-image:
    linear-gradient(rgba(18, 18, 18, 0.5), rgba(18, 18, 18, 0.8)),
    url('images/dark-studio.jpg');
```
记得同时修改文字颜色为浅色！

---

需要更多帮助？查看 README.md 或重新运行 Claude Code！
