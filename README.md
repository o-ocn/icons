# 🌐 Icons 图标库

个人精心收集与整理的高清网站图标库（Web Favicons & Logos）。  
通过 **GitHub Pages** 与 **jsDelivr CDN** 全球分发，专为新标签页快捷方式、博客导航、个人主页及书签工具提供无跨域限制（CORS-free）的高清直链。

🌐 **在线图库导航**：[https://o-ocn.github.io/icons/](https://o-ocn.github.io/icons/)

---

## ⚡ CDN 直链调用方式

每个图标均提供两种公网直链访问方式：

1. **GitHub Pages 直链**（海外及国际网络首选，永远同步最新仓库）：
   ```text
   https://o-ocn.github.io/icons/icons/{filename}
   ```
2. **jsDelivr CDN 直链**（国内访问更稳定，全球边缘节点缓存）：
   ```text
   https://cdn.jsdelivr.net/gh/o-ocn/icons@main/icons/{filename}
   ```

---

## 📋 图标总览与备注

| 图标预览 | 名称 | 分辨率 / 格式 | 官方网址 | Pages 直链 | jsDelivr CDN 直链 | 备注说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| <img src="icons/vmiss.png" width="48" height="48" alt="VMISS" /> | **VMISS** | 512×512 <br>`PNG` | [app.vmiss.com](https://app.vmiss.com/) | [🔗 直链](https://o-ocn.github.io/icons/icons/vmiss.png) | [⚡ CDN](https://cdn.jsdelivr.net/gh/o-ocn/icons@main/icons/vmiss.png) | VMISS 官方标志 Logo |

---

## 🛠️ 如何添加新图标

1. 将图标文件（`.png` / `.svg` / `.webp`）放入 `icons/` 目录；
2. 在 `data/icons.json` 中添加该图标的条目元数据；
3. 更新 `README.md` 表格；
4. 运行 `git commit` 并 `git push` 到 `main` 分支，GitHub Pages 将在 30 秒内自动生效！
