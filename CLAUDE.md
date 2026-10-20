# AnBoWork 工作台博客 - CLAUDE.md

Jekyll 静态博客，托管于 GitHub Pages（`gyabevincent-debug.github.io`），AnBoWork 官方博客。

## 红线：Git 身份隔离

**本仓库只允许使用本账号自己的仓库级身份提交，绝不能落到机器上的全局身份。违反即重大事故。**

1. **第一次 commit 之前**先写仓库级身份，不能只靠一次性的 `git -c ...` 参数：

   ```bash
   git config --local user.name "gyabevincent-debug"
   git config --local user.email "gyabevincent-debug@users.noreply.github.com"
   # remote: git@github-anbowork:gyabevincent-debug/gyabevincent-debug.github.io.git
   ```

2. **每次** commit、amend、rebase、cherry-pick 之后，核对作者和提交者两栏都是本账号：

   ```bash
   git log --format='%h A:%an <%ae> | C:%cn <%ce>' -5
   ```

3. **push 之前再核对一次**，不一致就不推送，先修好。
4. push 之后用公开接口复核：`https://api.github.com/repos/gyabevincent-debug/gyabevincent-debug.github.io/commits` 与 `/contributors`，只能出现本账号。
5. **本文件和仓库里所有文件都是公开的**：禁止写入任何个人真实姓名、其他账号的用户名或邮箱。
6. 一旦发现身份落错：立即停止并告知负责人。改写历史只能让分支干净，旧提交的哈希仍可被访问，彻底清除需要删库重建。

## 写文章

文件名 `_posts/YYYY-MM-DD-{slug}.md`（英文文章加 `en-` 前缀），front matter 含 title / date / lang / categories / tags / excerpt / description / image。
内容只写产品真实具备的功能，不夸大；产品信息以官网 https://www.anbowork.com 为准。

封面图统一用 AI 按正文内容生成（图中不放文字），存放在 `assets/images/covers/<slug>.webp`，尺寸 1200x630。
