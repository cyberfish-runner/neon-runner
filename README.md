# 霓虹跑者 NEON RUNNER

赛博朋克风格的 **2D 横版平台跳跃游戏**。霓虹冲刺、二段跳、全息闪烁平台、限时激光门、横移/升降平台、电网与节拍激光阵列，三关完整流程共 99 枚芯片。

- 🌐 **官方网站 / 在线试玩**：https://cyberfish-runner.netlify.app/
- ⬇️ **下载 Windows 版**：见本仓库的 [Releases](../../releases) 页面
- 🖥 **平台**：Windows 10（1809+）/ Windows 11，64 位
- 💰 **价格**：免费

本仓库只存放**官网页面**（纯静态 HTML/CSS）。游戏的 Windows 安装包与便携版作为 **Release 附件**分发，不放在仓库里。

## 目录结构

```
index.html            官网首页（单页，HTML + 内联 CSS，无 JS、无外部依赖）
play.html             游戏本体（在线试玩；与桌面版是同一份文件）
images/               截图、图标、社交分享封面
netlify.toml          Netlify 部署配置（缓存与安全响应头）
robots.txt            搜索引擎抓取规则
sitemap.xml           站点地图
```

## 本地预览

直接双击 `index.html` 即可（纯静态，`file://` 协议下也能玩）。
或者起个本地服务器：

```bash
python -m http.server 8080
# 然后打开 http://localhost:8080/
```

## 部署

推送到本仓库后，Netlify 会自动构建并发布（配置见 `netlify.toml`，发布目录为仓库根目录）。

---

**NEON RUNNER** · 免费游玩 · 请勿用于商业用途
