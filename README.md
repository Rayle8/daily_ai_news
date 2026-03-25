# 每日AI早报网站

每天自动生成的AI新闻早报网站，支持在线阅读和语音播报。

## 目录结构

```
daily-ai-news/
├── index.html              # 主页
├── news-YYYY-MM-DD.html   # 每日新闻内容
├── audio/
│   └── news-YYYY-MM-DD.mp3 # 每日语音播报
└── README.md
```

## 功能特点

- 📱 响应式设计，手机电脑都能看
- 🔊 点击播放按钮即可收听语音播报
- 📜 自动归档历史早报
- 🎨 简洁美观的界面
- 纯静态HTML，无需后端，可以部署到任何静态网站托管

## 部署方式

### GitHub Pages (免费)
1. 创建一个名为 `daily-ai-news` 的GitHub仓库
2. 推送所有文件：
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Daily AI News"
   git remote add origin https://github.com/你的用户名/daily-ai-news.git
   git push -u origin main
   ```
3. 在仓库设置中开启 GitHub Pages，选择 main 分支
4. 你的网站就会在 `https://你的用户名.github.io/daily-ai-news/` 上线

### Vercel (免费)
1. 导入Git仓库到Vercel
2. 直接部署，无需任何配置
3. 自动HTTPS，全球CDN加速

### 任何静态托管
直接把所有文件上传到你的服务器即可

## 每日更新流程

每天9点生成新闻后，自动更新：

1. 在 `index.html` 的 `newsArchive` 数组中添加新条目：
   ```javascript
   const newsArchive = [
       {
           date: "2026-03-26",
           title: "2026年3月26日 星期四",
           filename: "news-2026-03-26.html",
           audio: "audio/news-2026-03-26.mp3"
       },
       ... 之前的归档
   ];
   ```

2. 创建 `news-YYYY-MM-DD.html` 文件，写入HTML格式的新闻内容

3. 将语音文件保存为 `audio/news-YYYY-MM-DD.mp3`

4. 提交到Git并部署（如果使用CI/CD会自动更新）

## 本地预览

直接用浏览器打开 `index.html` 即可预览，不需要任何服务器。

