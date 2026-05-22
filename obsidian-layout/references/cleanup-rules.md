# 清理规则（Content Cleanup）

## 必须删除的内容

删除文章开头的 **YAML frontmatter 元数据块**（即以 `---` 开头和结尾包裹的整块区域）。

包括其中所有字段，例如：
- `author:`
- `source:`
- `url:`
- `saved:`
- `tags:`（frontmatter 内的）
- `id:`
- `title:`
- `date:`
- 以及其他同步工具（如 Readwise、Omnivore、Notion）自动生成的元数据字段

---

## 必须保留的内容

以下内容即使在 frontmatter 附近，也必须保留：

- 文中所有图片链接（`![[图片]]` 或 `![](url)` 格式）
- 文末【参考文献】区块
- 文末【注脚】区块
- 正文中的 `#标签`（注意：这不是 frontmatter 里的 tags，是正文中独立的 hashtag）

---

## 常见坑

- **frontmatter 的 tags ≠ 正文 #标签**：frontmatter 块内的 `tags: [xxx]` 要删，正文里的 `#xxx` 要保留
- **不要把正文第一行的标题当 frontmatter 删掉**：只删 `---` 包裹的区域
- **Readwise/Omnivore 导出文章开头通常有大段元数据**，全部在 `---` 内，整块删除即可
