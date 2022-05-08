# AND组件


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| TimeFrame|float|0.0|如果两个输入在时间范围内都收到非零信号，则该项目将发送输出.如果设置为 0,则输入必须同时接收信号.|
| MaxOutputLength|int|200|输出字符串的最大长度.注意：较大的值可能会导致内存使用量过大或出现网络问题.|
| Output|string|"1"|满足条件时发送的信号. |
| FalseOutput|string|""|满足条件时发送的信号(如果为空,则不发送任何信号). |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)f


## 例子
```xml
<Item identifier="andcomponent" category="Electrical" Tags="smallitem,logic" maxstacksize="8" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <AndComponent canbeselected="true" />
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem items="screwdriver" type="Equipped" />
    <input name="signal_in1" displayname="connection.signalinx~[num]=1" />
    <input name="signal_in2" displayname="connection.signalinx~[num]=2" />
    <input name="set_output" displayname="connection.setoutput" />
    <output name="signal_out" displayname="connection.signalout" />
  </ConnectionPanel>
  [...]
</Item>
```