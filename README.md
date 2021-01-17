<p align="center">
 <h2 align="center">GitHub Readme Stats</h2>
 <p align="center">在你的 README 中获取动态生成的 GitHub 统计信息！</p>

# 特性

- [GitHub 统计卡片](#GitHub-统计卡片)
- [GitHub 更多置顶](#GitHub-更多置顶)
- [热门语言卡片](#热门语言卡片)
- [主题](#主题)
- [自定义](#自定义)
- [自己部署](#自己部署)

# GitHub 统计卡片

将这行代码复制到你的 markdown 文件中，就是如此简单！

更改 `?username=` 的值为你的 GitHub 用户名。

```md
[![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry)](https://github.com/CSTHenry/github-readme-stats)
```

_注: 等级基于用户的统计信息计算得出，详见 [src/calculateRank.js](../src/calculateRank.js)_

### 隐藏指定统计

想要隐藏指定统计信息，你可以调用参数 `?hide=`，其值用 `,` 分隔。

> 选项：`&hide=stars,commits,prs,issues,contribs`

```md
![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&hide=contribs,prs)
```

### 将私人项目贡献添加到总提交计数中

你可以使用参数 `?count_private=true` 把私人贡献计数添加到总提交计数中。

_注：如果你是自己部署本项目，私人贡献将会默认被计数，如果不是自己部署，你需要分享你的私人贡献计数。_

> 选项: `&count_private=true`

```md
![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&count_private=true)
```

### 显示图标

如果想要显示图标，你可以调用 `show_icons=true` 参数，像这样：

```md
![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&show_icons=true)
```

### 主题

你可以通过现有的主题进行卡片个性化，省去[手动自定义](#自定义)的麻烦。

通过调用 `?theme=THEME_NAME` 参数，像这样：

```md
![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&show_icons=true&theme=radical)
```

#### 所有现有主题

dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula

你可以预览[所有可用主题](../themes/README.md)或者签出[主题配置文件](../themes/index.js), 而且如果你喜欢, **你也可以贡献新的主题** :D

### 自定义

你可以通过使用 URL 参数的方式，为你的 `Stats Card` 或 `Repo Card` 自定义样式。

常用选项：

- `title_color` - 卡片标题颜色 _（十六进制色码）_
- `text_color` - 内容文本颜色 _（十六进制色码）_
- `icon_color` - 图标颜色（如果可用）_（十六进制色码）_
- `bg_color` - 卡片背景颜色 _（十六进制色码）_ **或者** 以 _angle,start,end_ 的形式渐变
- `hide_border` - 隐藏卡的边框 _(布尔值)_
- `theme` - 主题名称，从[所有可用主题](../themes/README.md)中选择
- `cache_seconds` - 手动设置缓存头 _（最小值: 1800，最大值: 86400）_
- `locale` - 在卡片中设置语言 _(例如 cn, de, es, 等等)_

##### bg_color 渐变

你可以在 bg_color 选项中提供多个逗号分隔的值来呈现渐变，渐变的格式是 :-

```
&bg_color=DEG,COLOR1,COLOR2,COLOR3...COLOR10
```

> 缓存的注意事项: 如果 fork 数和 star 数 少于 1k , Repo 卡片默认缓存是 4 小时 （14400 秒） ，否则是 2 小时（7200）。另请注意缓存被限制为最短 2 小时，最长 24 小时。

#### 统计卡片专属选项:

- `hide` - 隐藏特定统计信息 _(以逗号分隔)_
- `hide_title` - _(boolean)_
- `hide_rank` - _(boolean)_
- `hide_border` - _(boolean)_
- `show_icons` - _(boolean)_
- `include_all_commits` - 统计总提交次数而不是仅统计今年的提交次数 _(boolean)_
- `count_private` - 统计私人提交 _(boolean)_
- `line_height` - 设置文本之间的行高 _(number)_

#### Repo 卡片专属选项:

- `show_owner` - 显示 Repo 的所有者名字 _(boolean)_

#### 语言卡片专属选项:

- `hide` - 从卡片中隐藏指定语言 _(Comma seperated values)_
- `hide_title` - _(boolean)_
- `hide_border` - _(boolean)_
- `layout` - 在两个可用布局 `default` & `compact` 间切换
- `card_width` - 手动设置卡片的宽度 _(number)_

> :warning: **重要:**
> 如 [Percent Encoding](https://en.wikipedia.org/wiki/Percent-encoding) 所指定，语言名称应使用 uri 转义。
> (例: `c++` 应该是 `c%2B%2B`, `jupyter notebook` 应该是 `jupyter%20notebook`, 等.)

---

# GitHub 更多置顶

GitHub 更多置顶 允许你在使用 GitHub readme profile 时，在个人资料中置顶多于 6 个 repo 。

是的！你不再受限于置顶最多 6 个存储库了。

### 使用细则

复制粘贴这段代码到你的 README 文件中，并更改链接。

端点: `api/pin?username=CSTHenry&repo=github-readme-stats`

```md
[![ReadMe Card](https://github-readme-stats.csthenry.vercel.app/api/pin/?username=CSTHenry&repo=github-readme-stats)](https://github.com/CSTHenry/github-readme-stats)
```

### Demo

[![ReadMe Card](https://github-readme-stats.csthenry.vercel.app/api/pin/?username=CSTHenry&repo=github-readme-stats)](https://github.com/CSTHenry/github-readme-stats)

使用 [show_owner](#自定义) 变量将 Repo 所有者的用户名包含在内。

[![ReadMe Card](https://github-readme-stats.csthenry.vercel.app/api/pin/?username=CSTHenry&repo=github-readme-stats&show_owner=true)](https://github.com/CSTHenry/github-readme-stats)

# 热门语言卡片

热门语言卡片显示了 GitHub 用户常用的编程语言。

_注意：热门语言并不表示我的技能水平或类似的水平，它是用来衡量用户在 github 上拥有最多代码的语言的一项指标，它是 github-readme-stats 的新特性_

### 使用细则

将此代码复制粘贴到您的 `README.md` 文件中，并修改链接。

端点: `api/top-langs?username=CSTHenry`

```md
[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry)](https://github.com/CSTHenry/github-readme-stats)
```

### 隐藏指定语言

可以使用 `?hide=language1,language2` 参数来隐藏指定的语言。

```md
[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry&hide=javascript,html)](https://github.com/CSTHenry/github-readme-stats)
```

### 紧凑的语言卡片布局

你可以使用 `&layout=compact` 参数来改变卡片的样式。

```md
[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry&layout=compact)](https://github.com/CSTHenry/github-readme-stats)
```

### Demo

[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry)](https://github.com/CSTHenry/github-readme-stats)

- 紧凑布局

[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry&layout=compact)](https://github.com/CSTHenry/github-readme-stats)

---

### 全部 Demos

- 默认

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry)

- 隐藏指定统计

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&hide=contribs,issues)

- 显示图标

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&hide=issues&show_icons=true)

- 包含全部提交

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&include_all_commits=true)

- 主题

从[默认主题](#主题)中进行选择

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&show_icons=true&theme=radical)

- 渐变

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api?username=CSTHenry&bg_color=30,e96443,904e95&title_color=fff&text_color=fff)

- 自定义统计卡片

![Anurag's github stats](https://github-readme-stats.csthenry.vercel.app/api/?username=CSTHenry&show_icons=true&title_color=fff&icon_color=79ff97&text_color=9f9f9f&bg_color=151515)

- 自定义 repo 卡片

![Customized Card](https://github-readme-stats.csthenry.vercel.app/api/pin?username=CSTHenry&repo=github-readme-stats&title_color=fff&icon_color=f9f9f9&text_color=9f9f9f&bg_color=151515)

- 热门语言

[![Top Langs](https://github-readme-stats.csthenry.vercel.app/api/top-langs/?username=CSTHenry)](https://github.com/CSTHenry/github-readme-stats)

---

### 快速提示 (对齐 Repo 卡片)

你通常无法将图片靠边显示。为此，您可以使用以下方法：

```md
<a href="https://github.com/CSTHenry/github-readme-stats">
  <img align="center" src="https://github-readme-stats.csthenry.vercel.app/api/pin/?username=CSTHenry&repo=github-readme-stats" />
</a>
<a href="https://github.com/CSTHenry/convoychat">
  <img align="center" src="https://github-readme-stats.csthenry.vercel.app/api/pin/?username=CSTHenry&repo=convoychat" />
</a>
```

## 自己部署

#### [Check Out Step By Step Video Tutorial By @codeSTACKr](https://youtu.be/n6d4KHSKqGk?t=107)

因为 GitHub 的 API 每个小时只允许 5 千次请求，我的 `https://github-readme-stats.csthenry.vercel.app/api` 很有可能会触发限制。如果你将其托管在自己的 Vercel 服务器上，那么你就不必为此担心。点击 deploy 按钮来开始你的部署！

注意: 从 [#58](https://github.com/CSTHenry/github-readme-stats/pull/58) 开始，我们应该能够处理超过 5 千次的请求，并且不会出现宕机问题 :D

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/CSTHenry/github-readme-stats)

<details>
 <summary>设置 Vercel 的指导</summary>

1. 前往 [vercel.com](https://vercel.com/)
1. 点击 `Log in`
   ![](https://files.catbox.moe/tct1wg.png)
1. 点击 `Continue with GitHub` 通过 GitHub 进行登录
   ![](https://files.catbox.moe/btd78j.jpeg)
1. 登录 GitHub 并允许访问所有存储库（如果系统这样提示）
1. Fork 这个仓库
1. 返回到你的 [Vercel dashboard](https://vercel.com/dashboard)
1. 选择 `Import Project`
   ![](https://files.catbox.moe/qckos0.png)
1. 选择 `Import Git Repository`
   ![](https://files.catbox.moe/pqub9q.png)
1. 选择 root 并将所有内容保持不变，并且只需添加名为 PAT_1 的环境变量（如图所示），其中将包含一个个人访问令牌（PAT），你可以在[这里](https://github.com/settings/tokens/new)轻松创建（保留默认，并且只需要命名下，名字随便）
   ![](https://files.catbox.moe/caem5b.png)
1. 点击 deploy，这就完成了，查看你的域名就可使用 API 了！

</details>
