# Color组件


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| UseHSV|bool|false| 启用后,组件将信号从 HSV 转换为 RGB,其中红色是 0 到 360 之间的色调,绿色是 0 到 1 之间的饱和度，蓝色是 0 到 1 之间的值.|

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="colorcomponent" category="Electrical" Tags="smallitem,logic" maxstacksize="8" linkable="false" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <ColorComponent canbeselected="true" />
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <requireditem items="screwdriver" type="Equipped" />
    <input name="signal_r" displayname="connection.signalr" />
    <input name="signal_g" displayname="connection.signalg" />
    <input name="signal_b" displayname="connection.signalb" />
    <input name="signal_a" displayname="connection.signala" />
    <output name="signal_out" displayname="connection.signalout" />
  </ConnectionPanel>
  [...]
</Item>
```

