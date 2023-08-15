# 物品(Item)
# 示例物品
>示例物品可以在  
./plugins/RevivedLocyItem/Items/ExampleItem.yml查看，建议配合示例物品来阅读wiki!  
>注意节点大小写
  
# · name 节点
这个节点，你可以填写你的RPG物品名称！  
并且支持颜色代码！
>示例: name: '&a&l>> 测试物品 <<'

# · id 节点
这个节点，你可以填写你的RPG物品材质种类  
这里可以填写一个数字，你也可以填写物品的英文名!（这是由于1.8之后物品ID就不再被支持了）

但是高版本依然可以使用物品id(但是其实不全)
>示例①: id: 283  
>示例②: id: Diamond #钻石

# · CustomModelData 节点
这个节点，你可以填写你的CustomModelData以修改材质
注意：只有一点十四版本以上才可以使用
请填写一位数字
>示例①: CustomModelData: 7  

# · lore 节点
这个节点，你可以编辑你的RPG物品的描述(Lore)!  
书写方式如示例物品所示!  
这里支持颜色代码……

# · Options 节点
这个节点，你可以编辑物品的属性(功能类似背包编辑器)  
编辑格式:  
> 属性名 ~ 属性值

## 属性名: UNBREAKABLE
这项属性决定了该物品是否无限耐久!属性值可以填(true/false)    
true即为打开该属性，false即为关闭该属性    
示例:    
> UNBREAKABLE ~ true

## 属性名: HIDE_ENCHANTS
这项属性决定了是否隐藏物品的附魔属性的显示!属性值可以填(true/false)  
true即为打开该属性，false即为关闭该属性  
示例:  
> HIDE_ENCHANTS ~ true

## 属性名: HIDE_UNBREAKABLE
这项属性决定了是否隐藏物品的不损信息的显示!属性值可以填(true/false)  
true即为打开该属性，false即为关闭该属性  
示例:  
> HIDE_UNBREAKABLE ~ true

## 属性名: HIDE_ATTRIBUTES
这项属性决定了是否隐藏物品的属性的显示(如 "攻击伤害 +7")!属性值可以填(true/false)  
true即为打开该属性，false即为关闭该属性  
示例:  
> HIDE_ATTRIBUTES ~ true

## 属性名: HIDE_POTION_EFFECTS
这项属性决定了是否隐藏物品的药效的显示!属性值可以填(true/false)  
true即为打开该属性，false即为关闭该属性  
示例:  
> HIDE_POTION_EFFECTS ~ true

## 属性名: DAMAGE
这项属性可以修改物品的攻击力  
这个属性可以使用表达式和PlaceHolderAPI的变量    
示例:  
> DAMAGE ~ 100  
> DAMAGE ~ (2*10)/4  
> DAMAGE ~ (%vault_eco_balance%*2)/100

## 属性名: ATTACK_SPEED
这项属性可以修改物品的攻击速度(低版本不会生效)   
示例:  
> ATTACK_SPEED ~ 1

## 属性名: MAX_HEALTH
这项属性可以修改物品手持或穿戴时增加的血量   
示例:  
> MAX_HEALTH ~ 5

## 属性名: MOVE_SPEED
这项属性可以修改物品手持或穿戴时增加的移动速度  
示例:  
> MOVE_SPEED ~ 0.8

## 属性名: ARMOR_VALUE
这项属性可以修改物品手持或穿戴时增加的护甲值(?)  
示例:  
> ARMOR_VALUE ~ 5

## 属性名: LUCK_VALUE
这项属性可以修改物品手持或穿戴时增加的幸运值(?)  
示例:  
> LUCK_VALUE ~ 5

# · Enchantment 节点
这个节点，你可以编辑物品的原版附魔
编辑格式:  
> 附魔英文名~ 附魔等级  
>  
> 附魔英文名:  
ARROW_DAMAGE    
附魔：力量 (弓)    
ARROW_FIRE    
附魔：火焰附加 (弓)  
ARROW_INFINITE  
附魔：无限 (弓)  
ARROW_KNOCKBACK  
附魔：击退 (弓)  
BINDING_CURSE  
附魔：绑定诅咒  
DAMAGE_ALL  
附魔：锋利  
DAMAGE_ARTHROPODS  
附魔：节肢杀手  
DAMAGE_UNDEAD  
附魔：亡灵杀手  
DEPTH_STRIDER  
附魔：海底漫步  
DIG_SPEED  
附魔：效率  
DURABILITY  
附魔：耐久  
FIRE_ASPECT  
附魔：火焰附加  
FROST_WALKER  
附魔：冰霜行者  
KNOCKBACK  
附魔：击退  
LOOT_BONUS_BLOCKS  
附魔：时运  
LOOT_BONUS_MOBS  
附魔：抢夺  
LUCK  
附魔：海之眷顾  
LURE  
附魔：诱饵 (钓鱼杆)  
MENDING  
附魔：经验修补  
OXYGEN  
附魔：水肺  
PROTECTION_ENVIRONMENTAL  
附魔：保护  
PROTECTION_EXPLOSIONS  
附魔：爆炸保护  
PROTECTION_FALL  
附魔：摔落保护  
PROTECTION_FIRE  
附魔：火焰保护  
PROTECTION_PROJECTILE  
附魔：抛射物保护  
SILK_TOUCH  
附魔：精准采集  
SWEEPING_EDGE  
附魔：横扫  
THORNS  
附魔：荆棘  
VANISHING_CURSE  
附魔：消失诅咒  
WATER_WORKER  
附魔：水下速掘  
  
> 例子:  
> DAMAGE_ALL ~ 10  
> MENDING ~ 1  
> KNOCKBACK ~ 20  

# · Skills 节点
这个节点，你可以编辑物品的技能……  
> 格式:  
> 技能名 ~ 值名1=xxx;值名2=xxx;值名3=xxx;…… @触发条件  
>
> 已知触发条件: RIGHT(右键触发) / LEFT(左键触发)     
>  
> 例子:  
> command ~ command=/suicide;type=player; @RIGHT  
> 上面的例子就形成了一个右键执行玩家指令自杀的功能!
>
> 接下来，我会给你展示所有的技能名 及其 值名

## 技能名: audio
这个技能，可以给玩家播放一个音频(需要AudioBuffer插件支持)  
这个插件你可以在这里获取:  

https://www.mcbbs.net/thread-832205-1-1.html [√]  

> 值名: name / n —— 音乐的名称  
> 例子:  
> audio ~ n=TestMusic @RIGHT  
> 第二个例子:  
> audio ~ name=jinitaimei @RIGHT

## 技能名: command
这个技能，可以强制执行指令(控制台指令/玩家指令/op指令)  

> 值名: type / ty / t ——  指令的种类(填op是op指令，填player是玩家指令，填console是控制台指令)  
> 值名: command / cmd / c —— 指令的内容(支持papi变量)  
>
> 例子:  
> command ~ command=/suicide;type=player; @RIGHT  
> 第二个例子:  
> command ~ c=/op %player_name%;t=op; @RIGHT  

## 技能名: launch
这个技能，可以发射(火球/凋零头/箭……)

> 值名: type / ty / t ——  发射抛掷物的种类，见下面    
> 
> Arrow —— 箭  
> DragonFireball —— 龙火球  
> Egg —— 鸡蛋  
> EnderPearl —— 末影珍珠  
> Fireball —— 火球  
> FishHook —— 鱼竿  
> LargeFireball —— 巨型火球  
> LingeringPotion —— 喷射无属性药水  
> LlamaSpit —— 羊驼的口水  
> ShulkerBullet —— 潜影贝的子弹(可能会打到自己)  
> SmallFireball —— 小火球  
> Snowball —— 雪球  
> SpectralArrow —— 特效箭(比如毒箭)  
> SplashPotion —— 喷溅药水(?)  
> ThrownExpBottle —— 经验瓶  
> ThrownPotion —— 喷溅药水(?)  
> Trident —— 三叉戟  
> WitherSkull —— 凋零头  
> 
> 值名: damage / d / da / dg —— 造成的伤害(只有能造成伤害的投掷物才能这么搞，比如经验瓶就不行，支持papi)  
>
> 例子:  
> launch ~ type=FireBall;d=15 * %vault_balance% @RIGHT 

## 技能名: lightning
这个技能，可以遭雷劈，但是不疼
> 例子:  
> lightning ~ @LEFT

## 技能名: msg
这个技能，可以给玩家发送信息
> 值名: msg / m ——  信息    
> 例子:  
> msg ~ m=&7&l>> &b哈喽(,,･∀･)ﾉ゛@RIGHT

##技能名: near
这个技能，可以给附近的实体造成伤害
> 值名: damage / d / da / dg ——  造成的伤害(支持papi)  
> 值名: x  
> 值名: y  
> 值名: z  
> 以上三个值是以x、y、z的立方体为攻击范围，造成伤害     
> 例子:  
> near ~ d=20 * %player_health%;x=10;y=10;z=10 @RIGHT #给10x10x10范围的实体造成20点伤害  
> 该技能不会对Citizens插件的假人生效

## 技能名: particle
这个技能，可以在玩家的位置执行一个粒子效果组(这个粒子效果是在  
.//plugins//RevivedLocyItem//Particles文件夹里的)    

> 值名: name / n —— 粒子效果名称  
> 例子:  
> particle ~ n=HeadCircle @RIGHT

## 技能名: push
这个技能，可以给玩家一个推力      

> 值名: dh ——高度上的推力(通常3就很高了)  
> 值名: dp ——水平上的推力(通常1就很高了，负数往后推)  
> 例子:  
> push ~ dp=-1.6;dh=0.8 @LEFT

##技能名: reach
这个技能，可以凭空攻击一个很远很远的怪物      

> 值名: damage / d / dg / da —— 伤害(支持papi)  
> 值名: range / r —— 最大可以够到的范围  
>
> 例子:  
> reach ~ r=15;d=25 * %player_level% @LEFT

## 技能名: skill
这个技能，可以执行一个技能组(在  
.//plugins//RevivedLocyItem//Skills文件夹里的)   
为什么使用技能组(使用技能组的好处)?  
1.可以设置冷却时间  
2.可以每个技能之间有延迟      

> 值名: name / n —— 技能组名   
>
> 例子:  
> skill ~ name=ExampleSkillReach @LEFT

# · Heat/Hit 节点
在这个节点下，可以填写当玩家用RPG武器的技能成功攻击生物时造成的技能
注意：由于命名错误，在本插件1.3.3版本以后Heat和Hit这两个名字均可以使用
但是建议使用"Hit"
格式:  
> 技能名 ~ 值名1=xxx;值名2=xxx;值名3=xxx;…… @触发对象   
> 触发对象中 self 是自己，target是攻击对象   
注意：触发对象不是所有技能都有的，比如说攻击成功后播放音乐，只能播放给玩家  
>我们下面会特别说明哪些需要有触发对象……

## 击打技能名: audio
这个击打技能，可以让你成功攻击玩家后，给玩家播放音效  
该技能不需要填写触发对象  

(需要AudioBuffer插件支持)  
这个插件你可以在这里获取:  

https://www.mcbbs.net/thread-832205-1-1.html [√]  

> 值名: name / n —— 音频名  
>
> 例子:  
> audio ~ n=TestMusic

## 击打技能名: command
这个击打技能，可以让你成功攻击玩家后，给玩家强制执行指令  
该技能不需要填写触发对象  

> 值名: type / ty / t ——  指令的种类(填op是op指令，填player是玩家指令，填console是控制台指令)  
> 值名: command / cmd / c —— 指令的内容(支持papi变量)  
>
> 例子:  
> command ~ t=op;cmd=/kill %player_name%

## 击打技能名: lightning
这个击打技能，可以让你成功攻击玩家后，给玩家或者击打对象的位置显示一条没有伤害的雷电  
该技能"需要"填写触发对象  
>
> 例子:  
> lightning ~ @target  

## 击打技能名: line
这个击打技能，可以在你和被攻击的实体之间牵一条线  
该技能不需要填写触发对象  
> 值名: type / ty / t —— 线的粒子效果名称(见粒子效果组部分)    
>
> 例子:  
> line ~ t=FLAME  

## 击打技能名: msg
这个击打技能，可以在攻击后给玩家发送信息  
该技能不需要填写触发对象  
> 值名: msg / m —— 信息内容(可以用颜色代码)    
>
> 例子:  
> msg ~ msg=&a哈哈哈哈

## 击打技能名: particle
这个击打技能，可以在玩家或被攻击对象的位置执行一个粒子效果组(这个粒子效果是在  
.//plugins//RevivedLocyItem//Particles文件夹里的) 

该技能"需要"填写触发对象     

> 值名: name / n —— 粒子效果名称  
> 例子:  
> particle ~ n=HeadCircle @target

## 击打技能名: push
这个击打技能，可以给玩家一个推力   
该技能"需要"填写触发对象        

> 值名: dh ——高度上的推力(通常3就很高了)  
> 值名: dp ——水平上的推力(通常1就很高了，负数往后推)  
> 例子:  
> push ~ dp=-1;dh=1 @self





