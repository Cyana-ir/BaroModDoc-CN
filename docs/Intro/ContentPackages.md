# 内容包

内容包是文件的集合，用于定义 潜渊症 中存在的事物的许多属性。这包括 [物品](../ContentTypes/Item.md)，[结构](../ContentTypes/Structure.md)，[怪物](../ContentTypes/Character.md)，[随机事件](../ContentTypes/RandomEvents.md)，[关卡生成参数](../ContentTypes/LevelGenerationParameters.md)，[职业](../ContentTypes/Jobs.md) 等。您可以在 [内容类型](ContentTypes.md) 页面中查看内容包定义内容的完整列表。

默认情况下，游戏使用一个名为“Vanilla”的内容包。任何其他内容包都可以被视为对游戏内容的修改，即“mod”。

内容包主要由称为 XML 的格式的文本文件以及任何所需的纹理和声音组成。如果您以前没有使用XML格式的经验，请不要担心 - 即使它一开始看起来很吓人，但格式非常简单。有关更多详细信息，请参阅 [XML](XML.md) 页面。

您正在编辑的任何内容包都应在根目录中的`LocalMods`文件夹中找到，该目录可以在游戏文件中找到。要访问游戏文件，请右键单击 Steam 库中的 潜渊症，然后转到`管理`>`浏览本地文件`。

## 文件列表

文件列表是每个内容包的重要组成部分;它允许游戏知道要加载哪些其他XML文件以及每个文件的用途。对于任何给定的mod，其文件名将始终为 `filelist.xml`。[潜艇](../Editors/SubmarineEditor.md) 和 [人物](../Editors/CharacterEditor.md) 编辑器将为您的每个创作生成一个基本文件列表。

内容包的根元素具有以下属性：
- `name`：玩家在游戏中看到的此内容包的名称。
- `modversion`：mod 的版本号。通常，随着新版本的模组发布到创意工坊，这种情况会逐渐增加。目前，这只是一个提示，让模组制作者能够检查正在使用的模组版本。
- `gameversion`：此模组上次更新的版本号。游戏可以使用此功能来检测需要修改以使其向后兼容的模组。
- `corepackage`：此内容包是否是一个“核心”包, [在下文有单独介绍](#core-packages)。

然后，此根元素具有需要加载的每个内容 XML 文件的子元素。每个子元素的名称必须是 [内容类型](ContentTypes.md) 中列出的类型。

下面的示例由一个文件组成，该文件定义了一个 [物品文件](../ContentTypes/Item.md)。

```xml
<contentpackage name="Alien Wrench" modversion="1.0.0" gameversion="0.17.8.0" corepackage="false">
    <Item file="%ModDir%/alienwrench.xml" />
</contentpackage>
```

### 核心包

如果您不是进阶mod制作者，则可能不需要阅读本节。

大多数模组通常不是核心内容包，而是在Vanilla内容包中添加或修改内容（游戏的默认内容）。

核心包是包含使游戏运行所需的所有文件的包，而不仅仅是在另一个内容包之上添加一些额外的文件。一次只能选择一个核心包。

这种软件包适用于非常彻底的模组，需要完全禁用香草游戏的内容。通常，这不是你想要使用的，因为[覆盖](Overrides.md)通常就足够了，当我们进行更新以添加更多所需文件时，核心包mod可能会变得不兼容。