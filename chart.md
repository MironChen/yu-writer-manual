---
description: >-
  Yu Writer
  支持把表格数据以图表的方式来显示，目前支持柱型图、条形图、折线图、面积图、饼型图、圆环图等类型。要把表格以图表方式显示，只需在表格上方添加一个 @chart
  指令即可。
---

# 图表

{% hint style="warning" %}
**注意：**本章中的大部分央视均无法在 GitBook 上呈现，故全部附图（Coming soon）
{% endhint %}

## 柱型图和条形图

下面是一个典型的表格，然后在上面空出一行，再在上面输入 `@chart`。

`@chart`

| Category | Series 1 | Series 2 | Series 3 |
| --- | --- | --- | --- |
| Category 1 | 4.3 | 2.4 | 2 |
| Category 2 | 2.5 | 4.4 | 2 |
| Category 3 | 3.5 | 1.8 | 3 |
| Category 4 | 4.5 | 2.8 | 5 |

在右侧的即时预览面板或者预览窗口应该能看到表格以柱型图的形式显示。

### 指令参数

Yu Writer 指令允许添加参数，方法是在指令下方使用 `key: value` 的形式添加，比如：

```text
@chart
type: column
size: auto
```

也可以把所有参数连接成一行，然后写在指令后面的括号内（此功能尚未完成），比如：

```text
@chart(type=column, size=auto)
```

### chart 指令的通用参数

chart 指令有两个通用参数，分别是：

#### **type**

用于指定显示的图表类型。

| 值 | 作用 |
| --- | --- |
| column | 显示为柱型图（默认值） |
| line | 显示为折线图 |
| pie | 显示为饼型图 |
| donut | 显示为圆环图 |
| bar | 显示为条形图 |
| area | 显示为面积图 |

#### **size**

指定图表显示的大小。

| 值 | 作用 |
| --- | --- |
| auto | 根据显示区域自动调整图表大小（默认值） |
| x-large | 显示为特大图，约 720 像素 |
| large | 显示为大图，约 600 像素 |
| medium | 显示为中等图，约 480 像素 |
| small | 显示为小图，约 360 像素 |
| x-small | 显示为特小图，约 240 像素 |

### 柱型图和条形图支持的参数

#### **stack**

指定是否以堆栈方式来显示图表，可选值为 true 和 false，默认值是 false。

#### **space**

指定柱子之间的间距，值为一个正整数，单位是像素，默认值为 30（柱型图） 或者 15（条形图）。如果 stack 参数值为 true，则会忽略此参数。

### 使用指令参数调整柱型图的外观的例子

```css
@chart
size: large
space: 20
```

| Category | Series 1 | Series 2 | Series 3 |
| --- | --- | --- | --- |
| Category 1 | 4.3 | 2.4 | 2 |
| Category 2 | 2.5 | 4.4 | 2 |
| Category 3 | 3.5 | 1.8 | 3 |
| Category 4 | 4.5 | 2.8 | 5 |

### 使用指令参数调整条形图的外观的例子

```css
@chart 
type: bar
stack: true
size: small
```

| Category | Series 1 | Series 2 | Series 3 |
| --- | --- | --- | --- |
| Category 1 | 4.3 | 2.4 | 2 |
| Category 2 | 2.5 | 4.4 | 2 |
| Category 3 | 3.5 | 1.8 | 3 |
| Category 4 | 4.5 | 2.8 | 5 |

## 饼型图和圆环图

下面是饼型图的例子：

```css
@chart 
type: pie
```

| Qtr | Sales |
| --- | --- |
| 1st Qtr | 8.2 |
| 2nd Qtr | 3.2 |
| 3rd Qtr | 1.4 |
| 4th Qtr | 1.2 |

下面是圆环图的例子

```css
@chart 
type: donut
```

| Qtr | Sales |
| --- | --- |
| 1st Qtr | 8.2 |
| 2nd Qtr | 3.2 |
| 3rd Qtr | 1.4 |
| 4th Qtr | 1.2 |

## 折线图和面积图

下面是折线图的例子：

```css
@chart 
type: line
```

|  | Series 1 | Series 2 |
| --- | --- | --- |
| 1/5/02 | 32 | 12 |
| 1/6/02 | 32 | 12 |
| 1/7/02 | 28 | 12 |
| 1/8/02 | 12 | 21 |
| 1/9/02 | 15 | 28 |

### 折线图和面积图支持的参数

#### **point**

指定是否显示拐点，可选值有 true 和 false，默认是 false。

#### **smooth: true**

指定是否圆滑线条，可选值有 true 和 false，默认值是 false。

#### 下面是面积图的例子

```css
@chart 
type: area
point: true
smooth: true
```

|  | Series 1 | Series 2 |
| --- | --- | --- |
| 1/5/02 | 32 | 12 |
| 1/6/02 | 32 | 12 |
| 1/7/02 | 28 | 12 |
| 1/8/02 | 12 | 21 |
| 1/9/02 | 15 | 28 |



