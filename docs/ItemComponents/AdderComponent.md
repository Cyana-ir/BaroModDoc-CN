# Adder组件


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| ClampMax|float|999999.0|组件的输出被限制在此值以下. |
| ClampMin|float|-999999.0|组件的输出被限制在此值以上. |
| TimeFrame|float|0.0|组件必须在此时间范围内接收到两个输入的信号才能输出结果.如果设置为 0,则必须同时接收输入. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="addercomponent" category="Electrical" Tags="smallitem,logic" maxstacksize="8" linkable="false" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <AdderComponent canbeselected="true" />
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem items="screwdriver" type="Equipped" />
    <input name="signal_in1" displayname="connection.signalinx~[num]=1" />
    <input name="signal_in2" displayname="connection.signalinx~[num]=2" />
    <output name="signal_out" displayname="connection.signalout" />
  </ConnectionPanel>
  [...]
</Item>
```
