# 电子书站点模板（可二次开发）

这是一个基于 **GitHub Pages + JSON 数据驱动 + 前端实时搜索** 的静态电子书站点模板。

当前版本已清空原始电子书内容、赞赏记录与原项目信息，仅保留可运行的功能框架，方便你自行上传和维护数据。

---

## 功能特性

- 前端实时搜索（支持多关键词）
- 纯静态部署（可直接托管在 GitHub Pages）
- 双数据源降级机制：
  - 优先读取 `docs/all-books.json`
  - 失败时降级读取 `docs/books.json`
- 无后端依赖，维护简单

---

## 目录说明

- `docs/index.html`：站点首页（已改为简洁模板页）
- `docs/search.js`：前端搜索逻辑
- `docs/all-books.json`：主书籍数据源
- `docs/books.json`：备用书籍数据源
- `sponsors.md`：赞助说明页（已清空为模板）

---

## 数据格式

请按如下结构维护 JSON 数组：

```json
[
  {
    "title": "示例书名",
    "author": "示例作者",
    "category": "示例分类",
    "link": "https://example.com/book-download"
  }
]
```

字段说明：

- `title`：书名
- `author`：作者
- `category`：分类
- `link`：下载链接（建议使用 `https://`）

---

## 发布与同步（GitHub）

1. 将本项目推送到你的 GitHub 仓库
2. 在仓库 Settings → Pages 中选择从 `main` 分支的 `/docs` 目录发布
3. 后续每次提交都会自动同步更新页面

---

## 后续可扩展方向

- 增加后台录入页（管理 JSON）
- 分类筛选与排序
- 分页与懒加载
- UI 主题切换（浅色/深色）
- SEO 与访问统计增强
