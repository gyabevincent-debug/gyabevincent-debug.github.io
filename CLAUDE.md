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

## 多语言：默认英文，可切换中文

- 英文在站点根目录（`/`），中文在 `/zh/` 下。新增语言按同样方式加前缀。
- 文章按语言分目录：`_posts/en/YYYY-MM-DD-{slug}.md`、`_posts/zh/YYYY-MM-DD-{slug}.md`，**两种语言的 slug 和日期相同**，front matter 用 `lang: en|zh` 区分。
- 同一篇文章的两个版本靠 front matter 的 `ref`（写 slug）配对，页面（首页、关于）也一样。`ref` 用来生成 hreflang、sitemap 里的互链和侧栏的语言切换链接，写错了切换就会回到对方的首页。
- 中文文章要在 front matter 里写死 `permalink: /zh/YYYY/MM/DD/{slug}/`；英文文章用全局的 `/:year/:month/:day/:title/`。
- 站内互链用 `{% post_url en/YYYY-MM-DD-slug %}` / `{% post_url zh/YYYY-MM-DD-slug %}`，只链同语言的文章。
- 英文文章是按英文写法写的，不是逐句翻译；产品事实以官网为准，两个语言版本不能互相矛盾。
- 界面文案在 `_data/i18n.yml`，导航在 `_data/navigation.yml`，两个文件里的语言键（`en` / `zh`）要一一对应；不要在布局里写死某种语言的文字。
- `feed.xml`（英文）、`zh/feed.xml`、`sitemap.xml` 是自己写的模板，所以没有启用 jekyll-feed / jekyll-sitemap / jekyll-seo-tag；`<head>` 里的标题、描述、canonical、hreflang、Open Graph 和结构化数据都在 `_includes/head-seo.html`。
- 语言切换只是普通链接，没有按浏览器语言自动跳转（对搜索引擎和读者都更稳）。
- 官网链接带语言：英文用 `https://www.anbowork.com/...`，中文用 `https://www.anbowork.com/zh/...`。

## 写文章

front matter 含 title / date / lang / ref / categories / tags / excerpt / description / image（中文文章再加 permalink）。`description` 同时是 meta description，控制在 160 字符以内（中文 80 字以内）。
内容只写产品真实具备的功能，不夸大；产品信息以官网 https://www.anbowork.com 为准。
文章里不写「规避制裁 / 地域限制 / 平台风控」这类说法，也不保证某个平台一定可用、账号不被处理。

封面图统一用 AI 按正文内容生成（图中不放文字），存放在 `assets/images/covers/<slug>.webp`，尺寸 1200x630。图里没有文字，所以英文和中文版本共用同一张。
