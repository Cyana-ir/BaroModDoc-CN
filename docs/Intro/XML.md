# XML

潜渊症 的大部分内容都是在[XML文件](https://baike.baidu.com/item/可扩展标记语言)中定义的。如果您以前从未使用过这些代码文件，它们可能看起来令人生畏，但即使您从未进行过任何类型的编程，它们实际上也很容易理解。

XML 文件几乎可以被任何文本编辑器（甚至是记事本）编辑，但我们建议使用支持代码突出显示并能够指出文件中错误的文本编辑器。例如，[Notepad++](https://notepad-plus-plus.org/) 是一款支持 XML 代码突出显示的免费、易于使用的软件。其他不错的选择还有 [Sublime Text]https://sublimetext.com/) 和 [Visual Studio Code](https://code.visualstudio.com/) 。

XML 文件由元素组成，由开始标记和结束标记分隔。在 潜渊症 的案例中，元素可以是例如项目。此类元素可以定义如下：

```xml
<Item>
</Item>
```

正如您可能想象的那样，仅凭这一点不足以完全定义项目。

元素也可以具有属性，这些属性通常提供有关元素的一些附加信息。例如：

```xml
<Item identifier="alienwrench" name="Alien Wrench" variantof="wrench" scale="0.2">
</Item>
```

元素也可以具有子元素。基于上一个示例，我们可以添加一个确定项目的外观的子元素：`Sprite`

```xml
<Item identifier="alienwrench" name="Alien Wrench" variantof="wrench" scale="0.2">
  <Sprite texture="%ModDir%/alienwrench.png" sourcerect="0,0,256,112" depth="0.55" origin="0.5,0.1" scale="0.1" />
</Item>
```

请注意，在此示例中，是一个自闭合元素。如果不需要定义子元素，则可以选择省略结束标记，方法是直接在开始标记处的结尾结束标签，例如：`<Sprite />`

可以选择在顶部添加编码声明。它通常如下所示：
```xml
<?xml version="1.0" encoding="utf-8"?>
```

XML 还支持添加注释。这些是会被 潜渊症 忽略的文本块。它们可用于提示和助记。
```xml
<!-- 这是一条注释 -->
<Item ...>
```

## 潜渊症-相关 注意事项

- 在 潜渊症 中，所有 XML 文件都具有以下约束：
  - 除了编码声明之外，可能只有一个根元素。这是文件中出现的第一个元素;所有后续元素都必须是此元素的子元素。
  - 元素的所有属性都必须是唯一的。
- 当引用模组中的其他文件时，游戏会将字符串`%ModDir%`解释为模组所在的目录。这是允许模组在通过 Steam 创意工坊安装或通过服务器下载时移动到不同目录所必需的。
- 要引用其他mod中的文件，您可以使用字符串格式`%ModDir:[模组名称]%`，其中`[模组名称]`被替换为其他mod的名称。
