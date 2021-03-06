---
description: 介绍 Yu Writer 表格功能的使用。
---

# 表格

## 表格的手动录入

当在行首输入一个竖线加一个空格再加一个列标题，比如 `| item`，此时按下 `Tab` 键会自动补完下一个单元格，输入第二列标题变成 `| item | name`，反复按 `Tab` 键直至把所有标头完成，比如 `| item | name | count |`。此时按下 `Enter` 键会自动生成表格分隔行，形成如下：

```text
| item | name | count |
| ---- | ---- | ----- |
```

此时光标位于第二行末尾，再按下 `Enter` 键会自动生成新行，形成如下表格：

```text
| item | name | count |
| ---- | ---- | ----- |
|      |      |       |
```

## 移动光标

使用 `Tab` 键和 `Shift+Tab` 键可以在各单元格之间移动，在单元格录入数据后按 `Tab` 键会自动调整列宽，并把光标移动到下一个单元格，如果下一个单元格非空，其中的内容会自动被选上，方便修改。

在单元格按 `Enter` 键会让光标跳到下一行的该列单元格。 在最后一行的单元格内部按 `Enter` 键可以跳出表格区域。

## 插入新行

在行尾按下 `Enter` 键可以插入或者增加新行。

## 更多内容…（Coming soon）

「更多内容正在编写中」

