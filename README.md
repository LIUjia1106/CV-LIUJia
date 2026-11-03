# Jia Liu · 刘佳 个人主页

网站：<https://liujia.netlify.app/>

- 基于 [Hugo Blox](https://docs.hugoblox.com/) 的 academic-cv 模板，Hugo 版本 0.126.1。
- 我加了一套自定义的设计：橙到蓝的「热流」配色，以及几个自制版块（研究卡片、声子小实验、新闻时间线、旅行、随笔）。
- 网站内容几乎都写在 `content/` 里的 Markdown 文件中。每个文件开头两条 `---` 之间的部分叫 front matter（YAML 格式），按里面已有的格式改字段就行。

---

## 改完之后怎么上线

Netlify 会在 GitHub 仓库 `main` 分支有新提交时自动重新构建网站，一般一两分钟就能看到更新。

```bash
cd ~/Library/CloudStorage/OneDrive-HKUSTConnect/Homepage/AcademicWebsite/CV-LIUJia
git add -A
git commit -m "简单写一下改了什么"
git push
```

推送后按 **Cmd+Shift+R** 强制刷新网页。如果网站没变化，去 Netlify 后台的 **Deploys** 页面看构建日志。最常见的原因是 YAML 格式写错，见文末「编辑小贴士」。

---

## 速查表：想改什么 → 去哪里

| 想改的内容 | 文件 / 文件夹 |
| --- | --- |
| 名字、头衔、单位、社交链接、个人简介、研究兴趣 | `content/authors/admin/_index.md` |
| 头像 | `content/authors/admin/avatar.jpg`（直接替换，文件名不变） |
| 教育经历、工作 / 助教经历、奖项、技能和爱好 | `content/authors/admin/_index.md`（`education:` `work:` `awards:` `skills:`） |
| 首页各版块的顺序和文字（研究、论文、报告、新闻、生活预览、联系） | `content/_index.md` |
| 研究主题卡片（首页 Research） | `content/_index.md` 里的 `block: research-themes` |
| 研究项目详细页 | `content/project/<项目名>/index.md` |
| 论文 | `content/publication/<论文文件夹>/`（`index.md` + `cite.bib`） |
| 学术报告 | `content/event/<报告文件夹>/index.md` |
| 新闻 | `content/_index.md` 里的 `block: news-timeline` |
| 生活页：旅行、音乐、随笔、趣味小事 | `content/life.md` |
| 随笔文章 | `content/post/<文章文件夹>/index.md` |
| 简历 PDF（Download CV 按钮） | `static/uploads/resume.pdf`（英文）、`static/uploads/resume-zh.pdf`（中文） |
| 「Experience」页面的版块 | `content/experience.md`（内容本身仍在 `authors/admin/_index.md` 里改） |
| 导航栏菜单 | `config/_default/menus.yaml` |
| 网站标题、SEO 描述、页脚、配色名、日期格式 | `config/_default/params.yaml` |
| 图片素材（研究插图、旅行照片、首页背景） | `assets/media/` |
| 样式（颜色、间距、卡片效果） | `assets/css/custom.css`；主题色板在 `assets/css/themes/ember.css` |
| 自制版块的 HTML 模板（一般不用动） | `layouts/partials/blox/` |

还没填完的地方都标了 `TODO(Jia)`，或者写成 `[方括号占位符]`。在 VS Code 里全局搜索 `TODO(Jia)` 和 `'[`，就能逐个找到。

---

## 常见操作

### 新增一篇论文

1. 复制 `content/publication/` 下任意一个论文文件夹，改名，例如 `2027-jcp-xxx/`。命名习惯是「年份-期刊缩写-关键词」。
2. 修改 `index.md`：
   - `title`、`authors`：`admin` 代表自己，会自动加粗。
   - `date`：上线日期，决定排序。
   - `doi`。
   - `publication_types`：期刊论文填 `article-journal`，预印本填 `article`。
   - `publication`：期刊名、卷、页码。
   - `summary`：卡片上显示的一句话。
   - `featured: true`：加了这一项，论文会出现在首页「Featured Publications」。
   - `image.filename`：配图，路径相对于 `assets/media/`。
3. 把 `cite.bib` 换成这篇论文的 BibTeX，网页上的 Cite 按钮会用它。
4. （可选）在 `content/_index.md` 的新闻里加一条。如果属于某个研究主题，也在 `research-themes` 那张卡片的 `papers:` 里加一个链接。

### 新增一次学术报告

复制 `content/event/` 下的一个文件夹，改名，然后修改 `index.md` 里的这几项：

- `title`、`event`（会议全称）、`location`、`date`、`summary`
- 想分享幻灯片的话，把 PDF 放到 `static/uploads/`，再填 `url_slides: 'uploads/xxx.pdf'`。

### 新增一条新闻

在 `content/_index.md` 里找到 `block: news-timeline`，在 `items:` 的**最上面**加一条：

```yaml
        - date: Mar 2027
          icon: newspaper
          text: "一句话新闻，可以用 [链接](publication/xxx/) 和 **加粗**。"
```

- 只显示最新的 `count` 条（目前 5 条），更早的会折叠到「Show earlier news」里。
- `icon` 用 [heroicons](https://heroicons.com/) 的图标名。目前用到的有：
  - `newspaper`、`document-text`（论文）
  - `microphone`（报告）
  - `academic-cap`（入学 / 毕业）
  - `trophy`（获奖）
  - `sparkles`（其他）

### 新增一个旅行目的地

1. 新建照片文件夹，例如 `assets/media/life/kyoto/`，把照片放进去。风景和美食照片可以混放；建议单张不超过 5 MB。
2. 打开 `content/life.md`，复制 `destinations:` 下面完整的一条 `- name:`（一直到它最后一张照片），粘贴到 `destinations:` 下方的**最上面**（最新的在前），然后修改：

```yaml
        - name: Kyoto
          date: Apr 2025
          emoji: ⛩️
          text: 几句话：走了哪条路、看到什么、吃到什么。
          photos:
            - image: life/kyoto/temple.jpg
              caption: 清水寺
            - image: life/kyoto/ramen.jpg
              caption: 一兰拉面
```

- 照片会自动裁成 4:3 的小图，点开能看原图。
- `image: ''` 留空时，会显示一个「Add a photo」的占位格子。
- 目的地多于一个时，页面顶部会自动出现目的地索引按钮。

### 写一篇随笔

1. 复制 `content/post/note-template/` 文件夹，改名，例如 `content/post/2026-11-first-note/`。
2. 修改 `index.md` 开头的这几项：
   - `title`
   - `summary`（卡片上显示）
   - `date`
3. 在第二个 `---` 下面写正文。
4. 想要封面图的话，在同一个文件夹里放一张 `featured.jpg`。
5. 写好后**删掉 `draft: true` 这一行**，否则不会发布。

发布的随笔会自动按日期出现在「生活」页的 Notes 版块，最新 3 篇显示在那里；全部随笔在 `/post/`。

### 音乐

修改 `content/life.md` 里 `id: music` 那一块的卡片文字。

想嵌入一个歌单播放器的话，把 `embed:` 填成以下任意一种地址（注释里有示例）：

- Spotify：Share → Embed playlist
- 网易云音乐：「生成外链播放器」

### 更新简历 PDF

用新文件替换 `static/uploads/resume.pdf`（英文）和 `static/uploads/resume-zh.pdf`（中文），**保持文件名不变**。首页的 Download CV 按钮和简介里的「中文简历」链接都会自动指向新文件。

### 修改个人信息 / 经历 / 奖项

都在 `content/authors/admin/_index.md` 里：

| 字段 | 内容 |
| --- | --- |
| `role`、`organizations` | 头衔和单位 |
| `profiles` | 邮箱、Google Scholar、ORCID、GitHub 等图标链接 |
| `interests` | 研究兴趣 |
| `education`、`work` | 教育经历、工作 / 助教经历。`date_start` / `date_end` 用 `2024-09-01` 这种格式；`date_end: ''` 表示至今 |
| `awards` | 奖项（只显示年份） |
| `skills` | 「Research toolkit」和「Off the clock」两组 |
| 文件末尾第二个 `---` 下面 | 首页的个人简介正文 |

### 研究主题和项目页

- 首页的四张研究卡片：改 `content/_index.md` 里 `block: research-themes` 的 `items:`。
- 点卡片进入的详细页：改 `content/project/<名字>/index.md`。
  - `weight` 决定在 Projects 页的排序，数字越小越靠前。
  - 配图放在 `assets/media/research/`。

### 菜单 / 首页版块顺序

- **导航栏菜单**：改 `config/_default/menus.yaml`。`weight` 越小越靠前；`/#news` 这种链接会跳到首页对应 `id` 的版块。
- **首页版块顺序**：在 `content/_index.md` 的 `sections:` 里整块上下移动，从一个 `- block:` 到下一个 `- block:` 之前算一整块。不想要的版块可以整块删掉。

---

## 文件夹结构

```
CV-LIUJia/
├── content/                  ← 网站内容（最常改）
│   ├── _index.md             首页所有版块
│   ├── life.md               生活页：旅行 / 音乐 / 随笔 / 趣味小事
│   ├── experience.md         经历页的版块布局
│   ├── projects.md           研究项目列表页
│   ├── authors/admin/        个人信息、简介、经历、奖项、技能、头像
│   ├── publication/          论文（每篇一个文件夹）
│   ├── event/                学术报告（每次一个文件夹）
│   ├── project/              研究项目详细页
│   └── post/                 随笔（note-template/ 是模板，草稿不会发布）
├── assets/
│   ├── media/                图片：research/ 研究插图，life/ 旅行照片，heat-lattice.svg 首页背景
│   └── css/                  custom.css 自定义样式；themes/ember.css 配色
├── static/uploads/           原样发布的文件：简历 PDF、幻灯片等
├── config/_default/          网站设置：params.yaml / menus.yaml / hugo.yaml
├── layouts/partials/blox/    自制版块模板（research-themes、phonon-playground、
│                             news-timeline、beyond-lab、travel-journal、notes-list）
├── netlify.toml              Netlify 构建设置（Hugo 版本）
└── go.mod                    Hugo Blox 模块版本（不要随意升级）
```

---

## 编辑小贴士（避免构建失败）

- **缩进只能用空格**，不能用 Tab，而且要和上下文对齐。
- **文字以 `[` 开头，或者包含 `: `（冒号加空格）时，整段要加引号**。例如 `text: '[占位]'`。单引号里如果要写英文撇号，要写成两个：`'It''s'`。
- 图片路径都**相对于 `assets/media/`**，例如 `life/kyoto/a.jpg`，不要写 `assets/media/`。
- `static/` 里的文件发布后地址里没有 `static`：`static/uploads/a.pdf` 对应的网址是 `/uploads/a.pdf`。
- 文件夹名请用英文小写和连字符，例如 `2027-jcp-xxx`；它会成为网址的一部分。
- 照片太大会拖慢构建速度。手机原图可以先导出为长边 2000–3000 像素的 JPG。
- 不确定的话先改一处、推送，在 Netlify 上确认构建成功，再继续改。

## 本地预览（可选）

不想每次都推送才能看到效果的话，可以在本机预览：

1. 安装 Hugo **extended 0.126.1**（需要和 `netlify.toml` 里的版本一致；版本太新可能不兼容）和 Go。
2. 在本文件夹运行 `hugo server`。
3. 打开 <http://localhost:1313/>。
