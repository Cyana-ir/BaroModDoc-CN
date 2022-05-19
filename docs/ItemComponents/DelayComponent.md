# DelayComponent


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| Delay|float|1.0|项目延迟信号多长时间（以秒为单位）. |
| ResetWhenSignalReceived|bool|false|当接收到新信号时，组件是否应丢弃先前接收到的信号. |
| ResetWhenDifferentSignalReceived|bool|false|当输入信号改变时，组件是否应该丢弃先前接收到的信号. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="delaycomponent" category="Electrical" Tags="smallitem,logic" maxstacksize="8" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true">
  <DelayComponent canbeselected="true" />
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem items="screwdriver" type="Equipped" />
    <input name="signal_in" displayname="connection.signalin" />
    <output name="signal_out" displayname="connection.signalout" />
    <input name="set_delay" displayname="connection.setdelay" />
  </ConnectionPanel>
  [...]
</Item>
```

