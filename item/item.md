# 物品(Item)
# 示例物品
>示例物品可以在  
./plugins/RevivedLocyItem/Items/ExampleItem.yml查看，建议配合实例物品来阅读wiki!  
>注意节点大小写
  
# · name 节点
这个节点，你可以填写你的RPG物品名称！  
并且支持颜色代码！
>示例: name: '&a&l>> 测试物品 <<'

# · id 节点
这个节点，你可以填写你的RPG物品材质种类  
这里可以填写一个数字，你也可以填写物品的英文名!
>示例①: id: 283  
>示例②: id: Diamond #钻石

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
> DAMAGE ~ (%vault_eco_balance% * 2) / 100

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