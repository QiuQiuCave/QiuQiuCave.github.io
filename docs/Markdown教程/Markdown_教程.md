#  Markdown教程
## 标题
要创建标题，使用<kbd>#</kbd>在标题文本前添加一到六个符号。<kbd>#</kbd>的数量将决定标题的层次结构和字体大小。
形如：
```
# 一级标题
## 二级标题
### 三级标题
……
###### 六级标题
```
## 文本样式
可以使用粗体、斜体、删除线、下标或上标文本来表示强调。

| Style | Syntax | Keyboard shortcut | Example | Output |
| --- | --- | --- | --- | --- |
| Bold加粗 | `** **` or `__ __`| <kbd>Command</kbd>+<kbd>B</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>B</kbd> (Windows/Linux) | `**This is bold text**` | **This is bold text** |
| Italic斜体 | `* *` or `_ _`     | <kbd>Command</kbd>+<kbd>I</kbd> (Mac) or <kbd>Ctrl</kbd>+<kbd>I</kbd> (Windows/Linux) | `_This text is italicized_` | _This text is italicized_ |
| Strikethrough删除线 | `~~ ~~` | None | `~~This was mistaken text~~` | ~~This was mistaken text~~ |
| Bold and nested italic粗体嵌套斜体 | `** **` and `_ _` | None | `**This text is _extremely_ important**` | **This text is _extremely_ important** |
| All bold and italic全部粗体斜体 | `*** ***` | None | `***All this text is important***` | ***All this text is important*** | <!-- markdownlint-disable-line emphasis-style -->
| Subscript下标 | `<sub> </sub>` | None | `This is a <sub>subscript</sub> text` | This is a <sub>subscript</sub> text |
| Superscript上标 | `<sup> </sup>` | None | `This is a <sup>superscript</sup> text` | This is a <sup>superscript</sup> text |

## 引用文本

使用 <kbd>></kbd> 实现文本引用。

```
> 这是一个引用示例
```
> 这是一个引用示例
> 
引用的文字会缩进，并采用不同的颜色。
## 引用代码
#### 行内代码引用
可以使用一对反引号 <kbd>`</kbd> 实现代码的行内引用：

```
就像`print('hello')`这样
```
就像`print('hello')`这样
#### 代码块
使用一对三重反引号<kbd>```</kbd>实现代码块，可以在前三个反引号后加代码的语言种类，实现代码的高亮：

\`\`\`

print('hello')

print('world')

\`\`\`

```python
print('hello')
print('world')
```

## 公式
Markdown支持Latex语法

可以使用一对<kbd>$</kbd>实现行内公式，

比如`$\alpha\$`,$\alpha$

使用一对三重<kbd>$</kbd>实现公式块，比如

```
$$
\dot{x}=Ax+Bu
$$
```
$$
\dot{x}=Ax+Bu
$$
