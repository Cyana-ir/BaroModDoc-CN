# connectionPanel


## 属性

| 属性|类型|默认值|描述 |
| ---|---|---|--- |
| Locked|bool|false|锁定的连接面板无法在游戏中重新接线. |

此组件还支持以下位置定义的属性: [ItemComponent](ItemComponent.md)


## 例子
```xml
<Item identifier="button" category="Electrical" tags="smallitem,button" cargocontaineridentifier="metalcrate" scale="0.5" impactsoundtag="impact_metal_light" isshootable="true" maxstacksize="8">
  <ConnectionPanel selectkey="Action" canbeselected="true" msg="ItemMsgRewireScrewdriver" hudpriority="10">
    <GuiFrame relativesize="0.2,0.32" minsize="400,350" maxsize="480,420" anchor="Center" style="ConnectionPanel" />
    <RequiredItem identifier="screwdriver" type="Equipped" />
    <output name="signal_out" displayname="connection.signalout" />
  </ConnectionPanel>
  <Holdable selectkey="Select" pickkey="Use" slots="Any,RightHand,LeftHand" msg="ItemMsgDetachWrench" PickingTime="10.0" aimpos="35,-10" handle1="0,0" attachable="true" attachedbydefault="true" aimable="true">
    <requireditem identifier="wrench" type="Equipped" />
  </Holdable>
  [...]
</Item>
```

