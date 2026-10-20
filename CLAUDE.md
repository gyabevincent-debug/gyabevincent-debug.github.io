# AnBoWork 工作台博客 — CLAUDE.md

Jekyll 静态博客，托管于 GitHub Pages（`gyabevincent-debug.github.io`），AnBoWork 官方博客。

## Git 身份（最高红线）

提交前必须使用 repo 级身份，不能用全局身份：

```bash
git config --local user.name "gyabevincent-debug"
git config --local user.email "gyabevincent-debug@users.noreply.github.com"
# remote: git@github-anbowork:gyabevincent-debug/gyabevincent-debug.github.io.git
```

## 写文章

文件名 `_posts/YYYY-MM-DD-{slug}.md`（英文文章加 `en-` 前缀），front matter 含 title / date / lang / categories / tags / excerpt / description。
内容只写产品真实具备的功能，不夸大；产品信息以官网 https://www.anbowork.com 为准。
