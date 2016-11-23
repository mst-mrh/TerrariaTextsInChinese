# TerrariaTextsInChinese

Terraria 游戏英文文本提取结果和汉化结果.

## 为什么会有这个Repo

Terraria 一直以来没有官方中文版, 无论是在游戏内无法用英文交流还是理解游戏方面, 都给玩家造成了麻烦.

民间汉化也无统一汉化, 关于文本/质量方面都有争议.

身为有略微洁癖的玩家, 我们准备做些什么以改善现状.

好在是官方有推出多语言支持的计划, 但并不知道何时支持…

我们致力打造一个基于玩家的中立汉化, 尽可能提高文本质量.

## 说明: 文本中变量格式

文本中含有一些可变量 (如NPC的名字, 玩家名等), 这些可变量默认用特定格式在文本中表示.

### 固定变量: `$VAR`

文本中Npc对话涉及到地图名称, 玩家名称等; 还有些提示文本按照键盘设置而变化.

示例: 
* `"There's no chefs in all of $Terraria.Main::worldName, so I have to cook all this fish myself! "`
* `"Press $Terraria.Main::cInv to access your crafting menu. ..."`

### 数组变量: `$VAR_INDEX`

文本中Npc对话涉及到其他Npc名称时会出现. 在`mapLegend`里还有一些物品名称会用到索引.

实例:
* `"Don't bother with $Npc_38, I've got all you need right here."`
* `"$Terraria.Main::itemName_63"`

### 条件文本: `[ $条件 ? 文本A : 文本B ]`

当条件成立时, 使用文本A; 若不成立则使用文本B.

示例:
* `"Double tap [ $Terraria.Main::ReversedUpDownArmorSetBonuses ? UP : DOWN ] to direct your guardian to a location"`
* `"Double tap [ $Terraria.Main::ReversedUpDownArmorSetBonuses ? UP : DOWN ] to call an ancient storm to the cursor location"`

### 随机文本: `[ 文本A | 文本B ]`

文本为随机出现时, 使用此种方式表示. 该语法不常用.

示例:
* `"[ Hmm? Nothing special today... just kidding! It's party time, and then it's after party time! | At last, my time has come! ]"`