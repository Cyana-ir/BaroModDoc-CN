# Afflictions 痛苦\影响  

<sup>相关文件: [[Shared:AfflictionsFile.cs]](https://github.com/Regalis11/Barotrauma/blob/master/Barotrauma/BarotraumaShared/SharedSource/ContentManagement/ContentFile/AfflictionsFile.cs) [[Shared:AfflictionPrefab.cs]](https://github.com/Regalis11/Barotrauma/blob/master/Barotrauma/BarotraumaShared/SharedSource/Characters/Health/Afflictions/AfflictionPrefab.cs)</sup>

*这是个自动生成(但人工翻译）的页面*

- **被核心包需求：** Yes



## Child elements 子元素
- `statuseffect`
- `statvalue`
- `abilityflag`
- `affliction`
- `icon`
- `afflictionoverlay`
- `effect`


## Attributes 属性
- `MinStrength` : `float`  | `最小强度` : `浮点数`  
- `MaxStrength` : `float`  | `最大强度` : ` 浮点数`  
- `MinVitalityDecrease` : `float`  | `最小生命值减少`：`浮点数`  
- `MaxVitalityDecrease` : `float`  | `最大生命值减少`：`浮点数`  
- `StrengthChange` : `float`  | `强度改变`：`浮点数`  
- `MultiplyByMaxVitality` : `bool`  | `是否随最大生命值增加`：`布尔变量（即true\false)`  
- `MinScreenBlur` : `float`  | `最小屏幕模糊`：`浮点数`  
- `MaxScreenBlur` : `float`  | `最大屏幕模糊`：`浮点数`
- `MinScreenDistort` : `float`  | `最小屏幕失真`：`浮点数`
- `MaxScreenDistort` : `float`  | `最大屏幕失真`：`浮点数`  
- `MinRadialDistort` : `float`  | `最小（视觉）径向畸变`：`浮点数`  
- `MaxRadialDistort` : `float`  | `最大（视觉）径向畸变`：`浮点数`  
- `MinChromaticAberration` : `float`  | `最小色象差`：`浮点数`  
- `MaxChromaticAberration` : `float`  | `最大色象差`：`浮点数`  
- `GrainColor` : `Color`  | 	`颗粒（视觉）颜色`：`RGB颜色值+亮度`  *ps:是视觉效果，详见井蛙之见的影响*  
- `MinGrainStrength` : `float`  | `最小颗粒（视觉）效果强度`：`浮点数`  
- `MaxGrainStrength` : `float`  | `最大颗粒（视觉）效果强度`：`浮点数`  
- `ScreenEffectFluctuationFrequency` : `float`  | `视觉效果波动频率`：`浮点数`  
- `MinAfflictionOverlayAlphaMultiplier` : `float`  |`最小影响图层透明度倍数`：`浮点数`  
- `MaxAfflictionOverlayAlphaMultiplier` : `float`  |`最小影响图层透明度倍数`：`浮点数`  *ps:这两条在目前版本（0.18.15.1）的afflictions.xml文件中并未出现，很可能翻译有误*  
- `MinBuffMultiplier` : `float`  | `最小增益倍数`：`浮点数`  
- `MaxBuffMultiplier` : `float`  | `最大增益倍数`：`浮点数`     *ps:效果可以参考“代谢缓慢”影响*  
- `MinSpeedMultiplier` : `float`  | `最小速度倍数`：`浮点数`  
- `MaxSpeedMultiplier` : `float`  | `最大速度倍数`：`浮点数`  
- `MinSkillMultiplier` : `float`  | `最小技能水平倍数`：`浮点数`  
- `MaxSkillMultiplier` : `float`  | `最大技能水平倍数`：`浮点数`    * ps:参考死神之税buff  
- `MinResistance` : `float`  |`最小抗性`：`浮点数`  
- `MaxResistance` : `float`  |`最大抗性`：`浮点数`      *ps:这个数应该介于0到1*  
- `DialogFlag` : `Identifier`  |`（设置）对话标识`：`一个识别用的字符串`  
- `Tag` : `Identifier`  |`设置标识`：`一个识别用字符串`  
- `MinFaceTint` : `Color`  |`最小面部色调`：`rgb+亮度`  
- `MaxFaceTint` : `Color`  |`最大面部色调`：`rgb+亮度`  
- `MinBodyTint` : `Color`  |`最小身体色调`：`rgb+亮度`  
- `MaxBodyTint` : `Color`  |`最小身体色调`：`rgb+亮度`   
*ps:此文件中所提及的color在xml中格式均为"int,int,int,int"，翻译来自游戏中对灯光颜色4值的理解。*  
*ps2:此文件中很多涉及最小最大的数值都是随* ***影响*** *本身的强度变化*

