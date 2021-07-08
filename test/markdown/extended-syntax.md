## 概述 :id=overview

约翰·格鲁伯 的原始设计文档中概述的[基本语法](basic-syntax)添加了许多日常所需的元素, 但对于某些人来说还不够. 这就是扩展语法的用武之地.

一些个人和组织通过添加其他元素 (如表格, 代码块, 语法突出显示, URL 自动链接和脚注) 来自行扩展基本语法. 这些元素可以通过使用基于基本 Markdown 语法的轻量级标记语言来启用, 或者通过向兼容的 Markdown 处理器添加扩展来启用.

## 适用性 :id=availability

并非所有 Markdown 应用程序都支持扩展语法元素. 您需要检查您的应用程序使用的轻量级标记语言是否支持您想要使用的扩展语法元素. 如果没有, 仍然可以在 Markdown 处理器中启用扩展.

### 轻量级标记语言 :id=lightweight-markup-languages

有几种轻量级标记语言是 Markdown 的超集. 它们包括 格鲁伯 的基本语法, 并通过添加其他元素 (如表格, 代码块, 语法突出显示, URL 自动链接和脚注) 来构建它. 许多最流行的 Markdown 应用程序使用以下轻量级标记语言之一:

- [CommonMark](https://commonmark.org)
- [GitHub 风格 Markdown (GFM)](https://github.github.com/gfm/)
- [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/)
- [MultiMarkdown](https://fletcherpenney.net/multimarkdown/)
- [R Markdown](https://rmarkdown.rstudio.com/)

### Markdown 工具 :id=markdown-processors

有 [数十个 Markdown 工具](https://github.com/markdown/markdown.github.com/wiki/Implementations)可供选择. 其中许多允许您添加启用扩展语法元素的扩展. 查看处理器的文档以获取更多信息.

## 表格 :id=tables

要添加表格, 请使用三个或更多连字符 `---` 创建每列的标题, 并使用竖线 `|` 分隔每列. 您可以选择在表的任一端添加管道.

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

渲染的输出如下所示:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

单元格宽度可以变化, 如下所示. 渲染的输出看起来是一样的.

```
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```

**提示:** 使用连字符和管道创建表格可能很乏味. 要加快流程, 请尝试使用 [Markdown 表格生成器](https://www.tablesgenerator.com/markdown_tables). 使用图形界面构建表格, 然后将生成的 Markdown

### 对齐 :id=alignment

您可以通过在标题行内的连字符的左侧, 右侧或两侧添加冒号 `:` , 将列中的文本向左, 向右或居中对齐.

```
| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here’s this |
| Paragraph |    Text     |    And more |
```

渲染的输出如下所示:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here’s this |
| Paragraph |    Text     |    And more |

### 表格中其他元素支持 :id=formatting-text-in-tables

您可以向表格中添加其他元素. 例如, 您可以添加 [链接](basic-syntax?id=links), [代码](basic-syntax?id=code) (仅反引号 `` ` `` 中的单词或短语, 而不是代码块) 和 [强调](basic-syntax?id=emphasis).

您不能添加标题, 块引用, 列表, 水平线, 图像或 HTML 标签.

### 转义表格中的管道字符 :id=escaping-pipe-characters-in-tables

您可以通过使用其 HTML 字符代码 `&#124;` 在表格中显示管道 `|` 字符

## 围栏代码块 :id=fenced-code-blocks

基本 Markdown 语法允许您通过将行缩进四个空格或一个制表符来创建 [代码块](basic-syntax?id=code-blocks). 如果您觉得这不方便, 请尝试使用围栏代码块. 根据您的 Markdown 处理器或编辑器, 您将在代码块前后的行上使用三个反引号 ` ``` ` 或三个波浪号 `~~~`. 优点? 您不必缩进任何行!

````
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

渲染的输出如下所示:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

**提示:** 需要在代码块内显示反引号? 请参阅 [转义字符](basic-syntax?id=escaping-characters) 以了解如何转义它们.

### 语法高亮 :id=syntax-highlighting

许多 Markdown 处理器支持围栏代码块的语法高亮显示. 此功能允许您为您的代码编写的任何语言添加颜色突出显示. 要添加语法突出显示, 请在围栏代码块之前的反引号旁边指定一种语言.

````
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````

渲染的输出如下所示:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## 脚注 :id=footnotes

脚注允许您添加注释和引用, 而不会弄乱文档正文. 创建脚注时, 在添加脚注引用的位置会出现一个带有链接的上标数字. 读者可以点击链接跳转到页面底部脚注的内容.

要创建脚注引用, 请在方括号 `[^1]`内添加插入符号和标识符. 标识符可以是数字或单词, 但不能包含空格或制表符. 标识符仅将脚注引用与脚注本身相关联——在输出中, 脚注按顺序编号.

在括号内使用另一个插入符号和数字添加脚注, 其中包含冒号和文本 (`[^1]: 我的脚注.`). 您不必在文档末尾放置脚注. 除了列表, 块引号和表格等其他元素之外, 您可以将它们放在任何地方.

```
这是一个简单的脚注,[^1] 这是一个更长的脚注. [^bignote]

[^1]: 这是第一个脚注.
[^bignote]: 这里包含多行段落和代码.

    也支持缩进段落.

    `{ my code }`

    添加任意数量的段落.
```

## 标题 ID :id=heading-ids

许多 Markdown 处理器支持[标题](basic-syntax?id=headings)的自定义 ID — 一些 Markdown 处理器会自动添加它们. 添加自定义 ID 允许您直接链接到标题并使用 CSS 修改它们. 要添加自定义标题 ID, 请将自定义 ID 括在与标题位于同一行的花括号中.

```text
### 我的标题 {#custom-id}
```

渲染的输出如下所示:

```html
<h3 id="custom-id">我的标题</h3>
```

### 链接到标题 ID :id=linking-to-heading-ids

通过创建带有数字符号 `#` 后跟自定义标题 ID 的[标准链接](basic-syntax?id=links), 您可以链接到文件中具有自定义 ID#的标题.

| Markdown                                      | HTML                                                     | Rendered Output                           |
| --------------------------------------------- | -------------------------------------------------------- | ----------------------------------------- |
| \[标题 ID\]\(extended-syntax?id=heading-ids\) | \<a href="extended-syntax?id=heading-ids"\>标题 ID\</a\> | [标题 ID](extended-syntax?id=heading-ids) |

其他网站可以通过将自定义标题 ID 添加到网页的完整 URL (例如`[标题 ID](extended-syntax?id=heading-ids)`) 来链接到该标题

## 定义列表 :id=definition-lists

某些 Markdown 处理器允许您创建术语及其相应定义的*定义列表*. 要创建定义列表, 请在第一行输入术语. 在下一行, 键入一个冒号, 后跟一个空格和定义.

```
第一项
: 这是第一个术语的定义.

第二项
: 这是第二项的一个定义.
: 这是第二项的另一个定义.
```

HTML 如下所示:

```html
<dl>
  <dt>第一项</dt>
  <dd>这是第一个术语的定义.</dd>
  <dt>第二项</dt>
  <dd>这是第二项的一个定义.</dd>
  <dd>这是第二项的另一个定义.</dd>
</dl>
```

渲染的输出如下所示:

<dl>
  <dt>第一项</dt>
  <dd>这是第一个术语的定义.</dd>
  <dt>第二项</dt>
  <dd>这是第二项的一个定义.</dd>
  <dd>这是第二项的另一个定义.</dd>
</dl>

## 删除线 :id=strikethrough

您可以通过在单词中心放置一条水平线来删除单词. 结果看起来像~~这样~~. 此功能允许您指出某些单词是错误的, 不应包含在文档中. 要删除单词, 请在单词前后使用两个波浪号 `~~`.

```
~~世界是平的.~~ 我们现在知道世界是圆的.
```

渲染的输出如下所示:

~~世界是平的.~~ 我们现在知道世界是圆的.

## 任务列表 :id=task-lists

任务列表允许您创建带有复选框的项目列表. 在支持任务列表的 Markdown 应用中, 内容旁边会显示复选框. 要创建任务列表, 请在任务列表项前添加破折号 `-` 和带空格 `[ ]` 的括号. 要选择复选框, 请在括号之间添加一个`x` (`[x]`).

```
- [x] 撰写新闻稿
- [ ] 更新网站
- [ ] 联系媒体
```

渲染的输出如下所示:

- [x] 撰写新闻稿
- [ ] 更新网站
- [ ] 联系媒体

## 表情符号 :id=emoji

有两种方法可以将表情符号添加到 Markdown 文件: 将表情符号复制并粘贴到 Markdown 格式的文本中, 或者输入*表情符号短代码*.

### 复制和粘贴表情符号 :id=copying-and-pasting-emoji

在大多数情况下, 您可以简单地从[Emojipedia](https://emojipedia.org/)等来源复制表情符号并将其粘贴到您的文档中. 许多 Markdown 应用程序会自动以 Markdown 格式的文本显示表情符号. 您从 Markdown 应用程序导出的 HTML 和 PDF 文件应显示表情符号.

**提示:** 如果您使用的是静态站点生成器, 请确保[将 HTML 页面编码为 UTF-8](https://www.w3.org/International/tutorials/tutorial-char-enc/).

### 使用表情符号短代码 :id=using-emoji-shortcodes

某些 Markdown 应用程序允许您通过输入表情符号短代码来插入表情符号. 它们以冒号开头和结尾, 并包含表情符号的名称

```text
去露营了! :tent: 早点回来。

那太有趣了! :joy:
```

渲染的输出如下所示:

去露营了! :tent: 早点回来。

那太有趣了! :joy:

**注意:** 您可以使用此[表情符号短代码列表](emoji), 但请记住, 表情符号短代码因应用程序而异. 有关更多信息, 请参阅 Markdown 应用程序的文档

## 自动 URL 链接 :id=automatic-url-linking

许多 Markdown 处理器会自动将 URL 转换为链接. 这意味着如果您输入 http://www.example.com, 即使您没有[使用括号](basic-syntax?id=links), 您的 Markdown 处理器也会自动将其转换为链接.

```
http://www.example.com
```

渲染的输出如下所示:

[http://www.example.com](http://www.example.com)

## 禁用自动 URL 链接 :id=disabling-automatic-url-linking

如果您不希望自动链接 URL, 可以通过将 URL 表示为带反引号的 [代码](basic-syntax?id=code) 来删除链接

```
`http://www.example.com`
```

渲染的输出如下所示:

`http://www.example.com`
