# Icons 图标库项目状态档案 (PROJECT_STATE.md)

> 📌 **单一事实源声明**：本项目采用本文件作为项目当前状态的**唯一事实源（Single Source of Truth）**。  
> ⚠️ **强制规范**：**必须完整包含以下六大核心支柱（缺少任何一项视为不合格交接）**。任何新 AI 接手前必须首先阅读本文件，完成实质工作后必须更新本文件。

---

## 一、项目目标（为什么做 / 终态目标）
- **核心定位与痛点**：
  - 集中管理并维护个人高品质图标资产，解决此前 Loon、网络代理策略组、常用应用及 Web 仪表盘（如 TablissNG）图标画风杂乱、上游分散、部分上游原图失效、英文/拼音命名导致中文检索困难以及专属 VPS/服务图标缺失的问题。
- **长期终态目标**：
  - 构建 100% 本地自托管、风格统一、支持中英双语检索的 Loon 策略组/节点图标聚合库与分类分库；
  - 同时为各类个人 Web 仪表盘与应用提供高速可靠的 GitHub / jsDelivr CDN 高清图标直链；
  - 维护长期稳定的定制图标扩充管道（如 `loon/icons/custom/`）。

---

## 二、当前状态（做到哪里 / 运行事实）
- **当前阶段**：生产稳定 / 阶段完成闭环
- **当前版本与分支**：分支 `main`，远端同步状态零差异（与 `origin/main` 一致，工作树 clean）
- **核心组件运行事实**：
  - **精选图标资产**：物理本地库收录 **2,782 个精选图标**，涵盖国家地区旗帜、主流代理软件、数百家机场/服务商、常用国内与国际应用、表情包/动漫、游戏及地标；
  - **个人定制专属图标**：已入库高清 512×512 PNG，保存在 `loon/icons/custom/`：
    - [`vmiss.png`](loon/icons/custom/vmiss.png)（VMISS 官方透明 Logo）
    - [`glados.png`](loon/icons/custom/glados.png)（GLaDOS 官方后台 PWA 钛黑翠绿雷达图标）
    - [`glados_classic.png`](loon/icons/custom/glados_classic.png)（GLaDOS 经典蓝云声波白底方圆角图标）
    - [`suxin.png`](loon/icons/custom/suxin.png)（素心 Network 官方白底方圆角绅士西装图标）
    - [`suxin_dark.png`](loon/icons/custom/suxin_dark.png)（素心 Network 黑曜石深色绅士西装图标）
  - **Loon 订阅文件**：专注于维护个人唯一的全量精选聚合主库：
    - 全量聚合库：[`loon/loon.json`](loon/loon.json)（2,782 图标，100% 格式合法且支持中英双语检索）
  - **导入协议支持**：支持纯净直链手动导入及 iOS Safari 原生 `loon://import?iconset=...` URL Scheme 一键唤醒导入。

---

## 三、已完成事项（哪些已验证 / 成果证据）
- [x] **上游图标同步与本地化沉淀**：从 The Magic、离歌图标包（ligeicon）、彩色静态旗帜、fmz200 四大上游拉取完整物理图标资产，100% 保存在本地 `loon/icons/` 仓库中，摆脱对第三方图床可用性的依赖；
- [x] **个人定制服务图标入库**：处理官方高清 512×512 透明背景 PNG，以规范纯英文 `VMISS` 注册至全量主库；
- [x] **机场高清专属图标制作与入库 (GLaDOS & 素心)**：
  - **GLaDOS (`glados.cloud`)**：提取官方控制台 PWA 矢量资产与经典品牌形象，生成 512×512 高清 Squircle 图标（包含官方钛黑翠绿雷达版 `glados.png` 与经典蓝云声波版 `glados_classic.png`，替换并升级原低清 144×144 模糊版本）；
  - **素心 Network (`suxins.life`)**：提取官方矢量品牌 Logo（绅士西装双排扣线条），生成 512×512 高清 Squircle 图标（包含 The Magic 画风 A 白底方圆角 `suxin.png` 与黑曜石深色版 `suxin_dark.png`）；
  - 单个图标体积精细控制在 18~21KB，完全符合秒开与高分屏 Retina 渲染规范；
  - 在 `loon/loon.json` 中以【原英文-中文】双语规范完成注册（`GLaDOS-GLaDOS机场`、`GLaDOS-Classic-GLaDOS经典蓝云`、`SuXin-素心`、`SuXin-Dark-素心暗黑`）；
- [x] **风格画风治理与去重精简**：
  - 国旗统一采用**画风 C（扁平正方形彩色贴片）**，剔除 `ligeicon/01Country` 中画风杂乱的 75 个散装国旗；
  - 机场统一采用**画风 A（The Magic 原版方圆角 App Store 官方质感）**，剔除 `ligeicon/06jichang` 中 27 个手绘冲突版本，并剔除 `fmz200/Twoandz9` 中 91 个完全复制 The Magic 的冗余副本；
  - 清理主流应用冗余变体（16 个 Swiftgram 数字变体、旧版低清 VMISS、数字占位图）；
  - 累计物理删除冗余图标 **210 个**，全库精炼至 **2,782 个精选图标**；
- [x] **全量中英双语检索补齐**：
  - 针对国内应用拼音（如 `youkushipin-优酷视频`、`aiqiyi-爱奇艺`、`baidunetdisk-百度网盘`、`meituan-美团` 等）、策略组通用图标（如 `chaxun-查询`、`liuliang-流量`、`jichang-机场` 等）、各大机场服务（如 `Shutiao-薯条`、`Mojie-魔戒`、`Flowercloud-花云`、`Ytoo-歪兔`、`Naiyou-奶昔` 等）、代理核心及国际常用应用，全量补齐 **1,470 个**【原英文/原拼音-中文】双语标签；
  - 动漫/表情包全量统一增加中文前缀（如 `Doraemon-哆啦A梦`、`Shin-chan-蜡笔小新`、`Pokemon-宝可梦`、`Menhera-表情包`）；
  - 严格保持 `VMISS` 纯英文不加中文后缀；
- [x] **404 导入问题排查与修复**：彻底废弃已失效的 `https://www.nsloon.app/openloon/...` 协议，更新为原生 URL Scheme 与纯净 `.json` 直链；
- [x] **使用文档完善**：更新 [`README.md`](README.md)，提供一键导入唤醒链接、手动订阅地址及规范说明。

### 实测验证记录
- **Python JSON 语法校验**：`loon/loon.json` 经 Python `json.load()` 解析验证，语法 100% 正确；
- **图标数量与链接完整性**：`loon.json` 共收录 2,782 项，全量无死链；
- **Git 远端验证**：所有变更均已推送至 GitHub `origin/main`，Commit 记录完整，工作区保持 clean。

---

## 四、历史决策（为什么这么做 / 放弃过什么）
### 1. 关键技术决定与原因
- **国旗画风选定画风 C（扁平正方形贴片）** -> **原因**：色彩规范统一、视觉质感整齐，最适合代理工具中的节点标识；
- **机场画风选定画风 A（The Magic 方圆角）** -> **原因**：符合 iOS App Store 官方圆角质感，图标精致度最高，符合用户审美偏好；
- **检索命名采用【原英文/原拼音-中文】共存** -> **原因**：若直接用中文替换原英文，用户用拼音或习惯的英文关键字将无法搜出图标；双语共存（如 `youkushipin-优酷视频`、`US-美国`）确保中英文均能精准命中；
- **VMISS 保持纯英文** -> **原因**：系用户 VPS 商家名，用户明确要求不需要中文后缀；
- **本地化物理存储所有上游图标** -> **原因**：避免上游仓库删库、重命名或网络阻断导致用户本地 Loon 图标大面积失效或 404；
- **404 导入采用原生 Scheme 与纯净直链** -> **原因**：旧版 `nsloon.app` 网页跳转中间件已失效，Loon 原生已支持 `loon://import?iconset=<URL>` 以及直接在输入框粘贴 `.json` 直链。

### 2. 已尝试但已放弃的方案（★ 严禁后续 AI 重复踩坑）
- **放弃方案 1：使用 `https://www.nsloon.app/openloon/import?iconset=...` 网页唤醒协议**
  - *尝试背景*：早期 Loon 社区常用的网页一键导入跳转链接。
  - *失败/放弃原因*：该官方跳转页面已全面下线，点击必报网页 404；若将该完整 URL 误粘贴进 Loon 的图标订阅框，Loon 同样解析失败报 404。后续一律使用原生 Scheme 或纯净 `.json` 直链。
- **放弃方案 2：直接用中文单方面替换英文/拼音文件名作为 Name**
  - *尝试背景*：初版设想将所有英文国旗与拼音应用替换为纯中文。
  - *失败/放弃原因*：用户反馈使用拼音（如搜 `youku`）或英文（如搜 `usa`）时会完全搜索不到，必须严格采用【原英文/原拼音-中文】双语共存格式。

---

## 五、未完成事项（Bug / 风险 / 待确认）
### 1. 已知缺陷与技术债 (Known Issues)
- 暂无阻塞性 Bug。所有 5 套订阅文件格式均已实测通过。

### 2. 待确认与排查事项 (Open Questions)
- [ ] 用户在实际 iOS 设备上通过 Loon 测试导入与搜索体验的最终真机反馈；
- [ ] 后续若遇到生僻应用或私有机场需要定制调整中文译名，按需增补。

### 3. 边界约束与潜在风险
- 图标直链依赖 GitHub Raw (`raw.githubusercontent.com`) 或 GitHub Pages (`o-ocn.github.io`)，国内直连时受网络环境影响，若遇解析延迟可搭配代理或使用 Pages / CDN 加速。

---

## 六、下一步计划（从哪里继续 / 具体工作）
1. **后续新图标增补管道**：若用户有未收录的新机场、私有节点或定制应用图标需要入库，接手 AI 直接将处理好的 512×512 透明 PNG 放入 `loon/icons/custom/`，在 `loon/loon.json` 中登记【原名-中文】（若为 VPS 商家名则按用户指示保留纯英文），提交并推送；
2. **保持工作区 clean**：日常维护不增加冗余文档，以本文件与实际资产为唯一事实源。

---

## 附录：工程资产与安全规范
### 1. 关键文件与配置清单
| 路径 | 宿主 / 仓库 | 用途说明 |
| :--- | :---: | :--- |
| `loon/loon.json` | 独立仓 `icons` | 全量聚合主库（2,782 图标，双语检索） |
| `loon/icons/custom/vmiss.png` | 独立仓 `icons` | VMISS 官方高清定制图标（512×512 透明 PNG） |
| `loon/icons/custom/glados.png` | 独立仓 `icons` | GLaDOS 官方后台 PWA 钛黑翠绿雷达图标（512×512） |
| `loon/icons/custom/glados_classic.png` | 独立仓 `icons` | GLaDOS 经典蓝云声波白底方圆角图标（512×512） |
| `loon/icons/custom/suxin.png` | 独立仓 `icons` | 素心 Network 官方白底方圆角绅士西装图标（512×512） |
| `loon/icons/custom/suxin_dark.png` | 独立仓 `icons` | 素心 Network 黑曜石深色绅士西装图标（512×512） |
| `README.md` | 独立仓 `icons` | 仓库对外说明、使用指引与一键唤醒链接 |

### 2. 安全与凭据管理
- 本项目为公开纯静态资源仓库，**绝无任何 Secret、Token 或认证密钥**；
- 严禁在任何说明文档、配置或脚本中混入个人敏感信息。
