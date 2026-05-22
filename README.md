# Claude Skills

> 我的 Claude Skills 个人合集，持续更新。
> 每个 Skill 都是从真实工作场景中提炼的，拿来即用。

---

## 📦 Skills 列表

| Skill | 说明 |
|-------|------|
| [obsidian-article-layout](./obsidian-layout/) | Obsidian 文章排版，100% 保留原文，自动优化结构 |

---

## 🗒️ obsidian-article-layout

**一句话描述：** 把杂乱的文章整理成结构清晰的 Obsidian Markdown 笔记，原文一字不删。

#### 解决什么问题

从 Readwise、Omnivore、微信公众号等渠道收藏的文章，导入 Obsidian 后往往：

- 没有标题层级，一大段文字堆在一起
- 带有大量 YAML 元数据残留
- 重点不突出，关键信息淹没在段落里

这个 Skill 帮你一键解决以上问题。

#### 功能清单

| 功能 | 说明 |
|------|------|
| 自动生成标题结构 | 识别逻辑段落，提取二三级标题，最多三级 |
| 智能加粗 | 核心术语、关键结论、重要数据加粗，每段最多 3 处 |
| 清理元数据 | 自动删除 frontmatter YAML 块（author/source/tags 等） |
| 列表转换 | 顿号、分号并列句自动转为列表，叙述性内容保持原样 |
| 长段拆分 | 单段过长时按语义合理拆分，不删字不加字 |
| 中英混合处理 | 连续英文段落自动翻译为中文，零散术语保留英文 |
| Obsidian 兼容 | 完整保留 `[[内部链接]]`、`#标签`、代码块等语法 |
| 标点补全 | 原文缺失标点时按语义补充，不改变原意 |

#### 触发方式

对 Claude 说以下任意一句即可自动触发：

- "帮我排版这篇文章"
- "整理成 Obsidian 格式"
- "格式太乱了帮我整理一下"
- "加上标题结构"
- "提升一下这篇笔记的可读性"

#### 文件结构

```
obsidian-layout/
├── SKILL.md                        # 核心指令
├── references/
│   ├── english-handling.md         # 英文内容处理规则
│   └── cleanup-rules.md            # frontmatter 清理规则
└── assets/
    └── layout-examples.md          # 输入/输出对照示例
```

#### 安装方式

**方式一：Claude 桌面客户端（推荐）**

1. 在本页面 **Releases** 中下载 `obsidian-layout.skill` 文件
2. 双击该文件，Claude 桌面客户端会自动打开并弹出安装确认窗口
3. 确认内容无误后，点击右下角 **Add to library**
4. 安装完成，对 Claude 说"帮我排版这篇文章"即可触发

---

**方式二：Claude Code 终端安装**

打开终端，执行以下命令：

```bash
git clone https://github.com/seabird000/claude-skills.git ~/.claude/skills/obsidian-layout
```

执行完毕后重启 Claude Code，Skill 自动生效。

---

## License

MIT © seabird000
