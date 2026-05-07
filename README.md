# Lavendulin KnowledgeHub

个人知识管理中心，基于 Claude Design Language 构建的静态站点，部署于 GitHub Pages。

**在线访问：** https://eevinci.github.io/knowledgeHub/

---

## 板块结构

```
├── 文段解析       深度思考与结构化整理（21篇归档）
├── 金融知识       行为金融学 · 市场心理学（每日 09:00 / 14:00 更新）
├── A股分析        AI上下游产业链 · 黄金珠宝板块（每日 08:00 更新）
├── 每日日记       个人每日记录
└── Skills 管理    工具能力 · 流程规范 · 扩展安装（13个 skill，点击可查看详情）
```

---

## 技术规格

| 项目 | 值 |
|---|---|
| 框架 | 纯 HTML/CSS/JavaScript，无构建依赖 |
| 标题字体 | Playfair Display / Georgia（衬线） |
| 正文字体 | Inter（无衬线） |
| 数据/代码字体 | JetBrains Mono |
| 主色调 | 赤陶色 `#C9544E` |
| 配色方案 | 赤陶色 + 黑白灰，不超过 3 种颜色 |
| 部署平台 | GitHub Pages（`/knowledgeHub` 子路径） |
| 设计语言 | Claude Design Language |

---

## 内容管理流程

Hub 内容通过 Hermes Agent 管理，更新链路：

```
修改本地文件（/workspace/hub-v2/）
    → mcp_matrix_deploy 部署
    → 自动推送 GitHub 仓库
    → GitHub Pages 自动构建（约1-2分钟生效）
    → 飞书推送链接 + 一句话摘要
```

**Hub 是唯一总入口**，不再单独维护索引页。

---

## 自动化定时任务

| 任务 | 时间 | 内容 |
|---|---|---|
| 每日金融知识 | 09:00 / 14:00 | 行为金融学 · 市场心理学，每日2篇 |
| A股早报 | 08:00 | AI上下游 + 黄金珠宝板块分析 |
| 文段解析 | 实时 | 用户发来的文字内容自动归档 |

---

## 维护规范

- Token / Key 等敏感信息以占位符存储，不出现明文
- 所有对外交付物统一使用 Claude Design Language
- 禁止 emoji，统一用 SVG 图标
- 子板块 index 链接路径：相对于自身，不含父级目录前缀

---

## 本地开发

```bash
# 克隆仓库
git clone https://github.com/EEvinci/knowledgeHub.git
cd knowledgeHub

# 直接在浏览器打开 index.html 即可预览
# （本地无需服务器，纯静态文件）
```

---

*Last updated: 2026-05-07*
