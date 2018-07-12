---
description: 有时文档的内容就是幻灯片的内容，那么为什么要重复劳动再做一个 PPT 呢？Yu Writer 支持以幻灯片的形式播放文档。
---

# 幻灯片及演示播放

{% hint style="warning" %}
**注意：**由于 GitBook 不支持幻灯片演示，故您需要下载本章的 Markdown 文件。下载后请在 Yu Writer 中打开进行演示。
{% endhint %}

## 见证魔术的时刻

现在就点击工具栏上的 `View` 按钮然后选择 `Toggle Presentation` 开始播放幻灯片吧！

## 书写上的约定

如果要制作美观的幻灯片，只需遵循很少的书写的约定即可。其中最基本的是：每个二级标题就会形成一张新的幻灯片。

## 支持的元素

* 字体格式（粗体、斜体等）
* 列表
* 图片
* 表格、图表
* 脚注
* 数学公式
* 语法加亮的代码块

其实所有文档支持的元素都能在幻灯片上显示 😄。

## 两栏式

作为幻灯片，一页内容不宜过长，文字尽量简明扼要。通常用两栏式可以容纳更多的内容。

如果要用两栏式，只需用分隔符 `- - -` 分开两部分即可。

比如接下来的图片将会显示在右栏。

「photo」

## 显示表格的例子

| Category | Series 1 | Series 2 | Series 3 |
| --- | --- | --- | --- |
| Category 1 | 4.3 | 2.4 | 2 |
| Category 2 | 2.5 | 4.4 | 2 |
| Category 3 | 3.5 | 1.8 | 3 |
| Category 4 | 4.5 | 2.8 | 5 |

在表格下方仍可以添加说明文字。

## 显示图表的例子

```css
@chart
type: pie
size: small
```

| Qtr | Sales |
| --- | --- |
| 1st Qtr | 8.2 |
| 2nd Qtr | 3.2 |
| 3rd Qtr | 1.4 |
| 4th Qtr | 1.2 |

* 图表指令 `@chart` 的参数依然可用；
* 如果一页的内容过长，可以通过滚动条查看一屏幕显示不完的内容；
* 所以，其实放长篇代码块也是没问题的。

## 所以这里来一段代码

```css
.slide-style {
  font-family: $viewFontFamily;
  font-size: 24px;
  line-height: 1.5em;

  h1, h2, h3, h4, h5, h6 {
    font-weight: 500;
    line-height: 1.3em;
    color: rgba($viewFontColor, .8);
    margin-top: 24px;
    margin-bottom: 16px;
  }
}
```

使用滚动条就可以看到我了。

## 页面内容也可以留空，标题就会居中显示

## 设置背景图片

只要把图片代码的 `title` 部分写成 `background`，那么这幅图片就会自动变成全屏显示的背景。

「photo」

## 设置全部页面的背景图片

你可以在文档的 Front Matter 中使用 `background` 字段设置所有页面的背景图片或者背景色，比如

```css
background: images/black.jpg
---
```

或者

```css
background: #f1f1f2
---
```

有关 Front Matter 的内容，详细请参见 [Front Matter](front-matter.md)

## 套用幻灯片样式

返回文档编辑状态，然后点击工具栏的 `View` 再点击 `Toggle Slides` 可以一览所有页面的缩略图，同时还可以选择不同的幻灯片样式。

## 演示结束



