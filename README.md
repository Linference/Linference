<div align="center">

# Hi, I'm LIN KIT 👋

### `Linference` = **Lin** + **Inference**

澳门 · 濠江中学 · 学生开发者

把学到的东西做成能跑的作品：AI 学习工具 · 三维城市记忆 · 笔触渲染

[![GitHub](https://img.shields.io/badge/GitHub-Linference-181717?style=flat-square&logo=github)](https://github.com/Linference)
![Location](https://img.shields.io/badge/Macau-🇲🇴-2f9e44?style=flat-square)
![Focus](https://img.shields.io/badge/Focus-AI%20%C3%97%203D%20%C3%97%20CV-1c7ed6?style=flat-square)

</div>

---

## 🧭 关于我

我是 **LIN KIT**，澳门濠江中学的一名学生开发者。

我的项目基本围绕三条线：**怎么让 AI 真的帮人把东西学会**、**怎么用三维重建把一座城市的记忆留下来**、**怎么用算法把一张图重画成一段过程**。

比起做一个「看起来很酷的 demo」，我更在意它能不能交付：本地优先、出处可追溯、结果能导出、关键逻辑有测试。

- 🔭 目前在推进：**格致** · **途见 TUJIAN** · **StrokeScape**
- 🌱 正在补课：深度学习、数据结构与算法、计算机视觉
- 🧪 关注方向：3DGS、非真实感渲染（NPR）、Agent 工程化、本地优先软件
- ⚡ *Linference* = Lin + **Inference**：名字里就写着「让想法得出结论」

---

## 🚀 主要项目

### 🎓 AI × 学习

#### [格致 · education](https://github.com/Linference/education)

> 本地优先的 AI 学习工作室 —— 让 AI 站在**你自己的书上**说话。

- **五角色讲解 + 六维反馈**：同学 / 教师 / 学生 / 考官 / 研究伙伴，从准确性、条件、推理、表达、举例、迁移六个维度评价你的讲解，并给出下一步建议
- **证据驱动**：回答要指到「哪本书、哪一页」，找不到出处就明说；AI 分数不计入独立通过，保留人工复核
- **学习闭环**：自信度记录、错误侦探、证据地图、迁移挑战，以及函数 / 受力 / 概率实验
- **本地优先**：库就是一个普通文件夹，Markdown 是唯一真源；SQLite trigram 双索引解决中文全文检索
- `Electron` `Node.js` `TypeScript` `SQLite` `Typst` `DeepSeek Harness` · 当前 0.0.8

#### [math_model](https://github.com/Linference/math_model) · [在线文档](https://linference.github.io/math_model/)

> 数学建模多智能体论文生成系统：把赛题 PDF 丢进去，走完整个建模流程。

- **8 Agent 对抗协作**：审题 → 选方法 → 联网找数据 → Python 求解 → 可视化 → LaTeX 编译 → 三角色并行审稿
- **9 道 Subagent 独立质检门禁** + 反模式硬阻断 + 人工在环检查点
- 21 本参考手册、6 本算法 Cookbook、中英句式库与反模式知识库
- 覆盖国赛 CUMCM / 美赛 MCM / HiMCM
- `Python` `LaTeX` `Multi-Agent` · ★ 6

### 🌏 3D × 城市记忆

#### [途见 · TUJIAN · macaumemory](https://github.com/Linference/macaumemory) · [在线体验](https://macau-memory-linference.linjie20091027.chatgpt.site)

> 基于 3DGS 与 GMVR 的澳门文旅记忆系统 —— 看见一座城，留下每一处记忆。

- **三维城市地图**：建筑轮廓与高度、地形、景点、定位、步行与驾车路线
- **GMVR 建筑识别**：YOLO 检测 → DINOv2 特征检索 → 位置辅助排序 → 多照片一致性核验 → 人工确认归档
- **3DGS 实景浏览**：大三巴 **657,492** 个高斯点、完整三阶球谐系数，网页端实时渲染
- **数字人「小澳」**：语音合成 + 语音识别导览；支持为普通街巷建立永久编号与照片档案
- `PlayCanvas` `WebGPU` `YOLO` `DINOv2` `3DGS` `Vite`

#### [MacauSplat](https://github.com/Linference/MacauSplat)

> 把 3DGS 重建结果，变成带精确标注的建筑数据集。

- **核心洞见**：重建过程本来就产生了标注所需的相机位姿（COLMAP）与稀疏点云 —— 在三维空间定一次包围盒，投影到每一帧，就得到几何一致、零漏框、可稽核的二维标注
- **工程细节**：上轴由相机轨迹 PCA 推定（不假设世界 Y 轴向上）、严格模式要求 8 角点全可见、用 track 反查遮挡
- **可复核输出**：YOLO 标签 + 逐帧明细 + 免依赖 `qa.html` 复核表 + 可人工编辑的 `box.json`
- 159 项单元测试；8 个真实重建项目端到端验证
- `Rust` `Tauri` `COLMAP` `3DGS` · 基于 OOOSplat（Apache-2.0）的衍生作品

### 🎨 视觉 × 工具

#### [绘序成境 · StrokeScape](https://github.com/Linference/StrokeScape)

> 把静态图像，重构成可逐笔播放的绘画过程。

- **结构感知**：Sobel 梯度 + 结构张量估计边缘、切线方向与方向一致性
- **分层笔触**：铺底 → 塑形 → 勾线 → 细节，每笔独立记录、严格串行播放，最高 50 万笔
- **可控创作**：8 种笔刷、局部精修、逐笔时间轴、原图滑动对比
- **交付友好**：单文件离线 HTML、MP4、可继续编辑的 `.strokescape` 工程；普通 CPU 即可完成全流程
- `React 19` `TypeScript` `FastAPI` `OpenCV` `NumPy` `Canvas`

#### [DeepSeek-Studio](https://github.com/Linference/DeepSeek-Studio)

> 桌面端 DeepSeek AI 编程助手：缓存优化、常驻运行、稳定高效。

- 面向长时间编码会话的桌面形态，重点解决上下文缓存命中与进程常驻下的稳定性问题

---

## 🛠 技术栈

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-47848F?style=for-the-badge&logo=electron&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)

</div>

---

## 📈 GitHub

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=Linference&show_icons=true&hide_border=true&theme=tokyonight&locale=cn" alt="GitHub Stats" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Linference&layout=compact&hide_border=true&theme=tokyonight&locale=cn&langs_count=8" alt="Top Languages" />

</div>

---

<div align="center">

### 「先让它跑起来，再让它跑得漂亮。」

📮 想聊点什么：直接开一个 [Issue](https://github.com/Linference/Linference/issues)

</div>
