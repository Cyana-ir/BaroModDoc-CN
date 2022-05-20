# Button Terminal


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| Signals|string[]|new string[0]|按下相应按钮时发送的信号. |
| activatingitems|string|""|物品的ID或tag,当包含时,允许使用按钮.多个应用逗号分隔. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="alienterminal" category="Alien" Tags="smallitem,logic" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <ButtonTerminal activatingitems="smallalienartifact" canbeselected="true" msg="ItemMsgInteractSelect">
    <GuiFrame relativesize="0.25,0.2" style="ItemUI" anchor="Center" />
    <TerminalButton style="alienbuttongreen" />
    <TerminalButton style="alienbuttonred" />
  </ButtonTerminal>
  <ItemContainer capacity="1" canbeselected="true" hideitems="true" slotsperrow="1" uilabel="" allowuioverlap="true">
    <Containable items="smallitem" />
  </ItemContainer>
  <ConnectionPanel selectkey="Action" canbeselected="true" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem identifier="screwdriver" type="Equipped" />
    <output name="signal_out1" displayname="connection.signaloutx~[num]=1" />
    <output name="signal_out2" displayname="connection.signaloutx~[num]=2" />
  </ConnectionPanel>
  [...]
</Item>
```
