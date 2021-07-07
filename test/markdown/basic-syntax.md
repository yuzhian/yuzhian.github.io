## 概述

几乎所有 Markdown 应用程序都支持 约翰·格鲁伯 在原始设计文档中概述的基本语法. Markdown 工具之间存在细微的差异 - 本文将尽可能地标注这些存在差异的内容.

## 标题

将数学符号 `#` 添加到单词或者短语前, 以创建一个标题. 你使用的数字符号的数量应该与标题的级别相对应. 举个例子, 要创建一个三级标题(''), 就使用三个数字符号 `### 我的标题`.

| Markdown                 | HTML                       | Rendered Output          |
| ------------------------ | -------------------------- | ------------------------ |
| `# Heading level 1`      | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| `## Heading level 2`     | `<h2>Heading level 2</h2>` | <h2>Heading level 2</h2> |
| `### Heading level 3`    | `<h3>Heading level 3</h3>` | <h3>Heading level 3</h3> |
| `#### Heading level 4`   | `<h4>Heading level 4</h4>` | <h4>Heading level 4</h4> |
| `##### Heading level 5`  | `<h5>Heading level 5</h5>` | <h5>Heading level 5</h5> |
| `###### Heading level 6` | `<h6>Heading level 6</h6>` | <h6>Heading level 6</h6> |

### 替代语法

或者, 在文字下方添加任意数量的 `==` 来创建一级标题, 或者添加 `--` 来创建二级标题.

| Markdown                            | HTML                       | Rendered Output          |
| ----------------------------------- | -------------------------- | ------------------------ |
| Heading level 1<br/>=============== | `<h1>Heading level 1</h1>` | <h1>Heading level 1</h1> |
| Heading level 2<br/>--------------- | `<h2>Heading level 2</h2>` | <h2>Heading level 2</h2> |

### 标题最优实践

Markdown 工具不支持井号(#)和标题名称之间缺少空格. 为了兼容性, 请在数字符号和标题名称之间空一个空格.

| ✅ 这样做          | ❌ 不要这样做     |
| ------------------ | ----------------- |
| # Here's a Heading | #Here's a Heading |

为了兼容性, 还应该在标题前后放置空行.

| ✅ 这样做                                                                         | ❌ 不要这样做                                                             |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Try to put a blank line before...<br><br># Heading<br><br>...and after a heading. | Try to put a blank line before...<br># Heading<br>...and after a heading. |

## 段落

要创建段落, 请使用空行分隔一行或多行文本.

| Markdown                                                                                                | HTML                                                                                                                          | Rendered Output                                                                                           |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| I really like using Markdown.<br /><br />I think I'll use it to format all of my documents from now on. | \<p\>I really like using Markdown.\</p\><br /><br />\<p\>I think I'll use it to format all of my documents from now on.\</p\> | <p>I really like using Markdown.</p><p>I think I'll use it to format all of my documents from now on.</p> |

### 段落最优实践

除非 [段落在列表中](basic-syntax?id=列表中添加段落), 否则不要用空格或制表符缩进段落.

| ✅ 这样做                                                                                               | ❌ 不要这样做                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Don't put tabs or spaces in front of your paragraphs.<br><br>Keep lines left-aligned like this.<br><br> | &nbsp;&nbsp;&nbsp;&nbsp;This can result in unexpected formatting problems.<br><br>&nbsp;&nbsp;Don't add tabs or spaces in front of paragraphs. |

## 换行符

要创建一个换行符 (`<br>`), 可以使用两个或多个空格结束一行, 然后键入回车.

| Markdown                                                               | HTML                                                                       | Rendered Output                                                  |
| ---------------------------------------------------------------------- | -------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| This is the first line. &nbsp;&nbsp;<br />And this is the second line. | \<p\>This is the first line.\<br\><br />And this is the second line.\</p\> | <p>This is the first line.<br />And this is the second line.</p> |

### 换行符最佳实践

在几乎每个 Markdown 应用程序中, 您都可以使用两个或多个空格(通常称为"尾随空格")作为换行符, 但这是有争议的. 在编辑器中很难看到尾随空格, 许多人不小心或故意在每个句子后面加上两个空格. 出于这个原因, 您可能希望使用除尾随空格以外的其他内容作为换行符. 如果您的 Markdown 应用程序[支持 HTML](/basic-syntax/#html), 您可以使用`<br>` HTML 标签.

为了兼容性, 请在行尾使用尾随空格或 `<br>` 标记.

不建议使用另外两个选项. CommonMark 和其他一些轻量级标记语言允许您在行尾键入反斜杠换行, 但并非所有 Markdown 应用程序都支持这一点, 因此从兼容性的角度来看, 这不是一个很好的选择. 至少有几种轻量级标记语言在行尾不需要任何内容, 只需键入火车, 它们就会创建一个换行符.

| ✅ 这样做                                                                                                                                     | ❌ 不要这样做                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| First line with two spaces after. &nbsp;<br>And the next line.<br><br>First line with the HTML tag after.\<br\><br>And the next line.<br><br> | First line with a backslash after.\\<br>And the next line.<br><br>First line with nothing after.<br>And the next line.<br><br> |

## 强调

你可以通过把文字加粗或者倾斜来强调.

### 加粗

要加粗文本, 请在单词或短语前后添加两个星号或下划线. 要将单词中间加粗以进行强调, 请在字母周围添加两个不带空格的星号.

| Markdown                     | HTML                                      | Rendered Output            |
| ---------------------------- | ----------------------------------------- | -------------------------- |
| `I just love **bold text**.` | `I just love <strong>bold text</strong>.` | I just love **bold text**. |
| `I just love __bold text__.` | `I just love <strong>bold text</strong>.` | I just love **bold text**. |
| `Love**is**bold`             | `Love<strong>is</strong>bold`             | Love**is**bold             |

#### 加粗最佳实践

Markdown 工具不支持如何处理单词中间的下划线. 为了兼容性, 请使用星号将单词的中间加粗以进行强调.

| ✅ 这样做        | ❌ 不要这样做    |
| ---------------- | ---------------- |
| `Love**is**bold` | `Love__is__bold` |

### 倾斜

要使文本倾斜, 请在单词或短语前后添加一个星号或下划线. 要将单词中间的斜体显示为强调, 请在字母前后添加一个不带空格的星号.

| Markdown                               | HTML                                          | Rendered Output                      |
| -------------------------------------- | --------------------------------------------- | ------------------------------------ |
| `Italicized text is the *cat's meow*.` | `Italicized text is the <em>cat's meow</em>.` | Italicized text is the _cat’s meow_. |
| `Italicized text is the _cat's meow_.` | `Italicized text is the <em>cat's meow</em>.` | Italicized text is the _cat’s meow_. |
| `A*cat*meow`                           | `A<em>cat</em>meow`                           | A*cat*meow                           |

#### 倾斜最佳实践

Markdown 工具不支持如何处理单词中间的下划线. 为了兼容性, 请使用星号将单词中间的斜体表示为强调.

| ✅ 这样做    | ❌ 不要这样做 |
| ------------ | ------------- |
| `A*cat*meow` | `A_cat_meow`  |

### 加粗并倾斜

要同时加粗和倾斜, 请在单词或短语前后添加三个星号或下划线. 要将单词的中间加粗和斜体以强调, 请在字母周围添加三个不带空格的星号.

| Markdown                                  | HTML                                                          | Rendered Output                         |
| ----------------------------------------- | ------------------------------------------------------------- | --------------------------------------- |
| `This text is ***really important***.`    | `This text is <strong><em>really important</em></strong>.`    | This text is **_really important_**.    |
| `This text is ___really important___.`    | `This text is <strong><em>really important</em></strong>.`    | This text is **_really important_**.    |
| `This text is __*really important*__.`    | `This text is <strong><em>really important</em></strong>.`    | This text is **_really important_**.    |
| `This text is **_really important_**.`    | `This text is <strong><em>really important</em></strong>.`    | This text is **_really important_**.    |
| `This is really***very***important text.` | `This is really<strong><em>very</em></strong>important text.` | This is really**_very_**important text. |

#### 加粗和倾斜最佳实践

Markdown applications don't agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold and italicize the middle of a word for emphasis.
Markdown 工具不支持如何处理单词中间的下划线. 为了兼容性, 请使用星号将单词的中间加粗和斜体以进行强调.

| ✅ 这样做                                     | ❌ 不要这样做                                 |
| --------------------------------------------- | --------------------------------------------- |
| This is really\*\*\*very\*\*\*important text. | This is really\_\_\_very\_\_\_important text. |

## 块引用

要创建块引用, 请在段落前添加一个 `>`.

```
> Dorothy followed her through many of the beautiful rooms in her castle.
```

渲染结果如下:

> Dorothy followed her through many of the beautiful rooms in her castle.

### 多段引用

Blockquotes can contain multiple paragraphs. Add a `>` on the blank lines between the paragraphs.

块引用可以包含多个段落. 在段落之间的空行上加一个 `>`.

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染结果如下:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### 嵌套块引用

块引用可以嵌套. 在要嵌套的段落前使用 `>>`

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染结果如下:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### 带有其他元素的块引用

块引用可以包含其他 Markdown 格式的元素. 并非所有元素都可以使用 - 您需要进行试验以查看哪些元素有效.

```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

渲染结果如下:

> <h4 class="no-anchor">The quarterly results look great!</h4>
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> _Everything_ is going according to **plan**.

### 块引用最佳实践

为了兼容性, 在块引用前后放置空行.

| ✅ 这样做                                                                                         | ❌ 不要这样做                                                                               |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Try to put a blank line before...<br><br>> This is a blockquote<br><br>...and after a blockquote. | Without blank lines, this might not look right.<br>> This is a blockquote<br>Don't do this! |

## 列表

您可以将元素组织成有序和无序列表.

### 有序列表

要创建有序列表, 请把数字加句点添加到行前. 数字不必按数字顺序排列, 但列表会从数字 1 开始.

| Markdown                                                                                                                                                        | HTML                                                                                                                                                                                                                         | Rendered Output                                                                                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. First item<br/>2. Second item<br/>3. Third item<br/>4. Fourth item                                                                                           | \<ol\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ol\>                                                                                          | <ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>                                                      |
| 1. First item<br/>1. Second item<br/>1. Third item<br/>1. Fourth item                                                                                           | \<ol\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ol\>                                                                                          | <ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>                                                      |
| 1. First item<br/>8. Second item<br/>3. Third item<br/>5. Fourth item                                                                                           | \<ol\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ol\>                                                                                          | <ol><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ol>                                                      |
| 1. First item<br/>2. Second item<br/>3. Third item<br/>&nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br/>&nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br/>4. Fourth item | \<ol\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item<br/>\<ol\><br>\<li\>Indented item\</li\><br/>\<li\>Indented item\</li\><br/>\</ol\><br/>\</li\><br/>\<li\>Fourth item\</li\><br/>\</ol\> | <ol><li>First item</li><li>Second item</li><li>Third item<ol><li>Indented item</li><li>Indented item</li></ol></li><li>Fourth item</li></ol> |

#### 有序列表最佳实践

CommonMark 和其他一些轻量级标记语言允许您使用右括号 `)` 作为分隔符(如: `1) First item`), 但并非所有 Markdown 工具都支持这一点, 因此从兼容性的角度来看, 这不是一个很好的选择. 为了兼容性, 请仅使用句点.

| ✅ 这样做                       | ❌ 不要这样做                   |
| ------------------------------- | ------------------------------- |
| 1. First item<br>2. Second item | 1) First item<br>2) Second item |

### 无序列表

要创建无序列表, 请在行项目前添加破折号 `-`、星号 `*` 或加号 `+`. 缩进一项或多项以创建嵌套列表.

| Markdown                                                                                                                                                  | HTML                                                                                                                                                                                                                           | Rendered Output                                                                                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| - First item<br/>- Second item<br/>- Third item<br/>- Fourth item                                                                                         | \<ul\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ul\>                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                      |
| _ First item<br/>_ Second item<br>_ Third item<br/>_ Fourth item                                                                                          | \<ul\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ul\>                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                      |
| + First item<br/>+ Second item<br/>+ Third item<br/>+ Fourth item                                                                                         | \<ul\><br>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item\</li\><br/>\<li\>Fourth item\</li\><br/>\</ul\>                                                                                            | <ul><li>First item</li><li>Second item</li><li>Third item</li><li>Fourth item</li></ul>                                                      |
| - First item<br/>- Second item<br/>- Third item<br/>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br/>&nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br/>- Fourth item | \<ul\><br/>\<li\>First item\</li\><br/>\<li\>Second item\</li\><br/>\<li\>Third item<br/>\<ul\><br/>\<li\>Indented item\</li\><br/>\<li\>Indented item\</li\><br/>\</ul\><br/>\</li\><br/>\<li\>Fourth item\</li\><br/>\</ul\> | <ul><li>First item</li><li>Second item</li><li>Third item<ul><li>Indented item</li><li>Indented item</li></ul></li><li>Fourth item</li></ul> |

#### 用数字开始无序列表项

如果需要以数字后跟句点开始无序列表项, 可以使用反斜杠 `\` 来转义句点

| Markdown                                                   | HTML                                                                                                  | Rendered Output                                                             |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| - 1968\. A great year!<br/>- I think 1969 was second best. | \<ul\><br>\<li\>1968. A great year!\</li\><br/>\<li\>I think 1969 was second best.\</li\><br/>\</ul\> | <ul><li>1968. A great year!</li><li>I think 1969 was second best.</li></ul> |

#### 无序列表最佳实践

Markdown 工具不支持如何处理同一列表中的不同分隔符. 为了兼容性, 不要在同一个列表中混用分隔符 - 选取一个使用.

| ✅ 这样做                                                      | ❌ 不要这样做                                                   |
| -------------------------------------------------------------- | --------------------------------------------------------------- |
| - First item<br>- Second item<br>- Third item<br>- Fourth item | + First item<br>\* Second item<br>- Third item<br>+ Fourth item |

### 在列表中添加元素

要在列表中添加另一个元素同时保持列表的连续性, 请将元素缩进四个空格或一个制表符, 如以下示例所示.

**Tip:** 如果出现的情况与您预期的不同, 请仔细检查您是否将列表中的元素缩进了四个空格或一个制表符.

#### 列表中添加段落

```
* This is the first list item.
* Here's the second list item.

    I need to add another paragraph below the second list item.

* And here's the third list item.
```

渲染的输出如下所示:

- This is the first list item.
- Here's the second list item.

  I need to add another paragraph below the second list item.

- And here's the third list item.

#### 列表中添加块引用

```
* This is the first list item.
* Here's the second list item.

    > A blockquote would look great below the second list item.

* And here's the third list item.
```

渲染的输出如下所示:

- This is the first list item.
- Here's the second list item.

  > A blockquote would look great below the second list item.

- And here's the third list item.

#### 列表中添加代码块

[代码块](#code-blocks) 通常缩进四个空格或一个制表符. 当它们在列表中时, 缩进八个空格或两个制表符.

```text
1. Open the file.
2. Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3. Update the title to match the name of your website.
```

渲染的输出如下所示:

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

#### 列表中添加图片

```
1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

   ![Tux, the Linux mascot](https://d33wubrfki0l68.cloudfront.net/e7ed9fe4bafe46e275c807d63591f85f9ab246ba/e2d28/assets/images/tux.png)

3. Close the file.
```

渲染的输出如下所示:

1. Open the file containing the Linux mascot.
2. Marvel at its beauty.

   ![Tux, the Linux mascot](https://d33wubrfki0l68.cloudfront.net/e7ed9fe4bafe46e275c807d63591f85f9ab246ba/e2d28/assets/images/tux.png)

3. Close the file.

#### 列表中添加列表

您可以在有序列表中嵌套无序列表, 反之亦然.

```
1. First item
2. Second item
3. Third item
    - Indented item
    - Indented item
4. Fourth item
```

渲染的输出如下所示:

1. First item
2. Second item
3. Third item
   - Indented item
   - Indented item
4. Fourth item

## 代码

要将单词或短语表示为代码, 请将其括在反引号 `` ` `` 中

| Markdown                              | HTML                                               | Rendered Output                     |
| ------------------------------------- | -------------------------------------------------- | ----------------------------------- |
| At the command prompt, type \`nano\`. | At the command prompt, type \<code\>nano\</code\>. | At the command prompt, type `nano`. |

### 转义反引号

If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (\`\`).
如果要表示为代码的单词或短语包含一个或多个反引号, 则可以通过将单词或短语括在双反引号 ` `` ` 中来将其转义

| Markdown                                    | HTML                                               | Rendered Output                         |
| ------------------------------------------- | -------------------------------------------------- | --------------------------------------- |
| \`\`Use \`code\` in your Markdown file.\`\` | \<code\>Use `code` in your Markdown file.\</code\> | `` Use `code` in your Markdown file. `` |

### 代码块

要创建代码块, 请将该块的每一行缩进至少四个空格或一个制表符.

```
    <html>
      <head>
      </head>
    </html>
```

渲染的输出如下所示:

    <html>
      <head>
      </head>
    </html>

**Note:** 要创建不缩进的代码块, 请使用 [围栏代码块](/extended-syntax/fenced-code-blocks).

## 水平线

To create a horizontal rule, use three or more asterisks (`***`), dashes (`---`), or underscores (`___`) on a line by themselves.
要创建水平线, 请在一行上单独使用三个或更多星号 `***`、破折号 `---` 或下划线 `___`

```
***

---

_________________
```

这三个的渲染输出看起来相同:

---

### 水平线最佳实现

为了兼容性, 在水平线前后放置空行.

| ✅ 这样做                                                                           | ❌ 不要这样做                                                          |
| ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Try to put a blank line before...<br><br>---<br><br>...and after a horizontal rule. | Without blank lines, this would be a heading.<br>---<br>Don't do this! |

## 链接

要创建链接, 请将链接文本括在方括号中(例如, \[Duck Duck Go\]), 然后紧跟在括号中的 URL 后面(例如, \(https://duckduckgo.com\)).

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com).
```

渲染的输出如下所示:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com).

**Note:** To link to an element on the same page, see [linking to heading IDs](/extended-syntax/#linking-to-heading-ids).

### 标题

You can optionally add a title for a link. This will appear as a tooltip when the user hovers over the link. To add a title, enclose it in parentheses after the URL.
您可以选择为链接添加标题. 当用户将鼠标悬停在链接上时, 这将显示为工具提示. 要添加标题, 请将其括在 URL 后的括号中.

```
My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").
```

渲染的输出如下所示:

My favorite search engine is [Duck Duck Go](https://duckduckgo.com 'The best search engine for privacy').

### URL 和电子邮件地址

要将 URL 或电子邮件地址快速转换为链接, 请将其括在尖括号中

```
<https://www.markdownguide.org>
<fake@example.com>
```

渲染的输出如下所示:

<https://www.markdownguide.org><br/>
<fake@example.com>

### 强调链接

To [强调](#emphasis) 链接,请在方括号和圆括号前后添加星号. 要将链接表示为[代码](#代码), 请在括号中添加反引号

```
I love supporting the **[EFF](https://eff.org)**.

This is the *[Markdown Guide](https://www.markdownguide.org)*.

See the section on [`code`](#code).
```

渲染的输出如下所示:

I love supporting the **[EFF](https://eff.org)**.

This is the _[Markdown Guide](https://www.markdownguide.org)_.

See the section on [`code`](#code).

### 参考式链接

参考式链接是一种特殊的链接, 它使 URL 更易于在 Markdown 中显示和阅读. 参考样式链接由两部分构成:与文本保持内联的部分和存储在文件其他位置以使文本易于阅读的部分

#### 参考式链接的第一部分

参考式链接的第一部分由两组括号构成. 第一组括号将应显示为链接的文本括起来. 第二组括号显示一个标签, 用于指向您存储在文档其他位置的链接.

尽管不是必需的, 但您可以在第一组和第二组括号之间包含一个空格. 第二组括号中的标签不区分大小写, 可以包含字母、数字、空格或标点符号.

这意味着以下示例格式与链接的第一部分大致相同:

- `[hobbit-hole][1]`
- `[hobbit-hole] [1]`

#### 参考式链接的第二部分

参考样式链接的第二部分使用以下属性进行格式化

1. 括号中的标签, 后面紧跟一个冒号和至少一个空格(如, `[label]: `).
2. 链接的 URL, 您可以选择将其括在尖括号中.
3. 链接的可选标题, 可以用双引号、单引号或括号括起来.

这意味着以下示例格式对于链接的第二部分大致等效:

- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit lifestyles'`
- `[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit lifestyles)`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit lifestyles'`
- `[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit lifestyles)`

您可以将链接的第二部分放在 Markdown 文档中的任何位置. 有些人将它们放在它们出现的段落之后, 而其他人则将它们放在文档的末尾(如尾注或脚注).

#### 参考式链接整体示例

Say you add a URL as a [standard URL link](#links) to a paragraph and it looks like this in Markdown:
假设你添加一个 URL 作为一个段落的[标准 URL 链接](#链接), 它在 Markdown 中看起来像这样:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole](https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"), and that means comfort.
```

Though it may point to interesting additional information, the URL as displayed really doesn't add much to the existing raw text other than making it harder to read. To fix that, you could format the URL like this instead:
虽然它可能指向附加信息, 但显示的 URL 确实不会对现有的原始文本增加太多, 只会增加它的阅读难度. 要解决这个问题, 您可以将 URL 格式化如下:

```
In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends
of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to
eat: it was a [hobbit-hole][1], and that means comfort.

[1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"
```

在上述两种情况下, 渲染的输出将是相同的:

> In a hole in the ground there lived a hobbit. Not a nasty, dirty, wet hole, filled with the ends of worms and an oozy smell, nor yet a dry, bare, sandy hole with nothing in it to sit down on or to eat: it was a <a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a>, and that means comfort.

链接的 HTML 将是:

```
<a href="https://en.wikipedia.org/wiki/Hobbit#Lifestyle" title="Hobbit lifestyles">hobbit-hole</a>
```

### 链接最佳实践

Markdown 工具不支持如何处理 URL 中间的空格. 为了兼容性, 请尝试使用 URL encode 将空格编码为 `%20`

| ✅ 这样做                                             | ❌ 不要这样做                                     |
| ----------------------------------------------------- | ------------------------------------------------- |
| \[link\]\(https://www.example.com/my%20great%20page) | \[link\]\(https://www.example.com/my great page\) |

## 图像

To add an image, add an exclamation mark (`!`), followed by alt text in brackets, and the path or URL to the image asset in parentheses. You can optionally add a title after the URL in the parentheses.
要添加图像, 请添加感叹号 `!`, 后跟括号中的替代文本, 以及括号中图像资产的路径或 URL. 您可以选择在括号中的 URL 后添加标题.

```
![The San Juan Mountains are beautiful!](https://mdg.imgix.net/assets/images/san-juan-mountains.jpg "San Juan Mountains")
```

渲染的输出如下所示:

![The San Juan Mountains are beautiful!](https://mdg.imgix.net/assets/images/san-juan-mountains.jpg 'San Juan Mountains')

### 链接图像

为图像添加链接, 请将图像的 Markdown 括在括号中, 然后将链接添加在括号中.

```
[![An old rock in the desert](https://mdg.imgix.net/assets/images/shiprock.jpg)](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)
```

渲染的输出如下所示:

[![An old rock in the desert](https://mdg.imgix.net/assets/images/shiprock.jpg)](https://www.flickr.com/photos/beaurogers/31833779864/in/photolist-Qv3rFw-34mt9F-a9Cmfy-5Ha3Zi-9msKdv-o3hgjr-hWpUte-4WMsJ1-KUQ8N-deshUb-vssBD-6CQci6-8AFCiD-zsJWT-nNfsgB-dPDwZJ-bn9JGn-5HtSXY-6CUhAL-a4UTXB-ugPum-KUPSo-fBLNm-6CUmpy-4WMsc9-8a7D3T-83KJev-6CQ2bK-nNusHJ-a78rQH-nw3NvT-7aq2qf-8wwBso-3nNceh-ugSKP-4mh4kh-bbeeqH-a7biME-q3PtTf-brFpgb-cg38zw-bXMZc-nJPELD-f58Lmo-bXMYG-bz8AAi-bxNtNT-bXMYi-bXMY6-bXMYv)

## 转义字符

要显示原本用于格式化 Markdown 文档中文本的文字字符, 请在该字符前添加反斜杠 `\`.

```
\* Without the backslash, this would be a bullet in an unordered list.
```

渲染的输出如下所示:

\* Without the backslash, this would be a bullet in an unordered list.

### 可以转义的字符

您可以使用反斜杠来转义以下字符.

| Character | Name                                                                                                                         |
| --------- | ---------------------------------------------------------------------------------------------------------------------------- |
| \         | backslash                                                                                                                    |
| `         | backtick (see also [escaping backticks in code](https://www.markdownguide.org/basic-syntax/#escaping-backticks))             |
| \*        | asterisk                                                                                                                     |
| \_        | underscore                                                                                                                   |
| { }       | curly braces                                                                                                                 |
| [ ]       | brackets                                                                                                                     |
| < >       | angle brackets                                                                                                               |
| ( )       | parentheses                                                                                                                  |
| #         | pound sign                                                                                                                   |
| +         | plus sign                                                                                                                    |
| -         | minus sign (hyphen)                                                                                                          |
| .         | dot                                                                                                                          |
| !         | exclamation mark                                                                                                             |
| \|        | pipe (see also [escaping pipe in tables](https://www.markdownguide.org/extended-syntax/#escaping-pipe-characters-in-tables)) |

## HTML

许多 Markdown 应用程序允许您在 Markdown 格式的文本中使用 HTML 标签. 如果您更喜欢某些 HTML 标签而不是 Markdown 语法, 这会很有帮助. 例如, 有些人发现对图像使用 HTML 标签更容易. 当您需要更改元素的属性时, 使用 HTML 也很有帮助, 例如指定文本的颜色或更改图像的宽度.

要使用 HTML, 请将标签放在 Markdown 格式文件的文本中.

```
This **word** is bold. This <em>word</em> is italic.
```

渲染的输出如下所示:

This **word** is bold. This <em>word</em> is italic.

### HTML 最佳实践

For security reasons, not all Markdown applications support HTML in Markdown documents. When in doubt, check your Markdown application's documentation. Some applications support only a subset of HTML tags.

Use blank lines to separate block-level HTML elements like `<div>`, `<table>`, `<pre>`, and `<p>` from the surrounding content. Try not to indent the tags with tabs or spaces — that can interfere with the formatting.

You can't use Markdown syntax inside block-level HTML tags. For example, `<p>italic and **bold**</p>` won't work.

出于安全原因, Markdown 文档中, 并非所有 HTML 都被支持. 如有疑问, 请查看 Markdown 工具的文档. 某些应用程序仅支持 HTML 标记的一个子集.

在块级元素如 `<div>`, `<table>`, `<pre>`, 和 `<p>`前后使用空行. 尽量不要用制表符或空格缩进标签——这会干扰格式.

不能在块级 HTML 标签中使用 Markdown 语法. 例如, <p>italic and **bold**</p>不会生效.
