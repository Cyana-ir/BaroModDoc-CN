# Concat组件


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| MaxOutputLength|int|256|输出字符串的最大长度. 警告:较大的值可能会导致大量内存使用或网络负载. |
| Separator|string|""| |
| TimeFrame|float|0.0|此组件必须在此时间范围内接收到两个输入的信号才能输出结果. 如果设置为 0,则必须同时接收输入. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="concatcomponent" category="Electrical" Tags="smallitem,logic" maxstacksize="8" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <ConcatComponent canbeselected="true" />
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

