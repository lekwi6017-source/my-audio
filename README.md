# My Audio (for GitHub Pages)

这是一个用 **GitHub Pages** 托管音频文件的最小仓库。  

## 使用方法

### 1. 上传音频
把 `.mp3 / .ogg / .m4a` 文件放在 `audio/` 文件夹里，提交并推送：

```bash
git add audio/xxx.mp3
git commit -m "add new audio"
git push
```

### 2. 开启 GitHub Pages
在仓库 Settings → Pages：  
- Source 选 `Deploy from a branch`  
- Branch 选 `main`，Folder 选 `/ (root)`  
保存后几分钟就会生成一个 URL，例如：  

```
https://用户名.github.io/my-audio/
```

### 3. 获取音频直链
音频文件的路径就是：

```
https://用户名.github.io/my-audio/audio/文件名.mp3
```

例如：
```
https://用户名.github.io/my-audio/audio/song1.mp3
```

### 4. 在自己的网站中使用
把这个 URL 粘贴到你的“添加链接”功能里，即可跨设备播放。  

---

## 注意
- 保持 HTTPS，否则浏览器会拦截。
- 文件过大加载会慢，建议用 ffmpeg 压缩，例如：
  ```bash
  ffmpeg -i input.mp3 -b:a 128k output.mp3
  ```
- GitHub Pages 每天有流量上限（约 100GB），个人使用完全足够。
