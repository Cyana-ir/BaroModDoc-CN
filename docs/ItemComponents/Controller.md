# Controller


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| IsToggle|bool|false|启用后，该项目将连续发出一个 0/1 信号并与之交互将翻转信号（使该项目表现得像一个开关）。 禁用时，与该项目交互时将简单地发送 1. |
| State|bool|false|项目是否打开/关闭。 仅当 IsToggle 设置为 true 时才有效. |
| HideHUD|bool|true|选择此项目时是否应隐藏 HUD（库存、健康栏等）. |
| UsableIn|UseEnvironment|UseEnvironment.Both|可以在空中、水下还是两者都选择该项目. |
| DrawUserBehind|bool|false|是否应该将使用该物品的角色绘制在该物品的后面. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="periscope" tags="periscope" category="Machine,Weapon" type="Controller" disableitemusagewhenselected="true" scale="0.5" isshootable="true" requireaimtouse="false" requireaimtosecondaryuse="false">
  <Controller UserPos="-35.0, -50.0" direction="Right" canbeselected="true" msg="ItemMsgInteractSelect">
    <limbposition limb="Head" position="-10,-135" />
    <limbposition limb="Torso" position="-10,-200" />
    <limbposition limb="LeftHand" position="67,-170" />
    <limbposition limb="RightHand" position="67,-170" />
  </Controller>
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem items="screwdriver" type="Equipped" />
    <output name="position_out" displayname="connection.turretaimingout" fallbackdisplayname="inputtype.aim" />
    <output name="trigger_out" displayname="connection.turrettriggerout" fallbackdisplayname="inputtype.shoot" />
  </ConnectionPanel>
  [...]
</Item>
```

