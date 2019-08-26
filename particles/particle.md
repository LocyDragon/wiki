# 粒子效果组(Particles)
# 示例粒子效果组
>示例物品可以在  
./plugins/RevivedLocyItem/Particles/ExampleParticle.yml查看，建议配合示例粒子效果组来阅读wiki!  
>注意节点大小写
>
>请确保你已经阅读完 [Skills技能组] 相关内容!  

粒子效果组是什么？  
这个东西，可以让你在一个平面"直角坐标系"中画出一些粒子效果组，支持延迟  

## ! 粒子效果种类对应的英文名
EXPLOSION_NORMAL —— 普通爆炸  
EXPLOSION_LARGE —— 大爆炸  
FIREWORKS_SPARK —— 烟花火星  
BUBBLE —— 气泡  
SPLASH —— 水溅起来  
WAKE —— 钓鱼  
SUSPENDED —— 悬挂(?)  
SUSPENDED_DEPTH —— 深度悬挂(?)  
CRIT —— 暴击效果  
MAGIC_CRIT —— 魔法暴击(?)  
SMOKE —— 烟  
SMOKE_LARGE —— 巨大的烟团  
SPELL —— 喷溅药水  
SPELL_INSTANT —— 喷溅药水  
SPELL_MOB —— 喷溅药水  
SPELL_MOB_AMBIENT —— 信标  
WITCH_MAGIC —— 女巫的紫色魔法  
DRIP_WATER —— 水颗粒  
DRIP_LAVA —— 岩浆颗粒  
ANGRY_VILLAGER —— 村民生气的效果  
HAPPY_VILLAGER —— 开心的效果  
TOWN_AURA —— 菌丝  
NOTE —— 音符盒  
PORTAL —— 小黑传送  
ENCHANTMENT_TABLE —— 附魔台  
FLAME —— 烈焰人火焰  
LAVA —— 岩浆  
FOOTSTEP —— 脚步(?)  
CLOUD —— 云  
REDSTONE —— 红石  
SNOWBALL —— 扔出雪球  
SNOW_SHOVEL —— 铲雪  
SLIME —— 史莱姆  
HEART —— 爱心  
BARRIER —— 屏障  
ITEM_CRACK —— 使用物品(?)  
BLOCK_CRACK —— 使用方块(?)  
BLOCK_DUST —— 方块的尘土  
WATER_DROP —— 水滴  
ITEM_TAKE —— 一种神奇还见不到的颗粒(1.13移除)  
MOB_APPEARANCE —— 远古守卫者  
END_ROD —— 末地烛  
DRAGON_BREATH —— 龙息  
DAMAGE_INDICATOR —— 打中生物，掉血  
SWEEP —— 横扫

# · origin 节点
这个节点代表了你的坐标系原点所在的玩家的相对位置  
比如 origin: (0,2,0) ——这样子所有粒子效果都会往上移动2格  
通常使用origin: (0,0,0)  
> 使用方法:  
> origin: (x,y,z)  
> 
> 示例:  
> origin: (0,0,0)

# · amount 节点
这个节点的值越大，每一颗粒子效果看上去就会越聚集
> 示例:  
> amount: 5

# · offsetX / offsetY / offsetZ 节点
这三个节点通常设置为0，改变这三个节点，粒子的位置会发生轻微移动。
> 示例:  
> offsetX: 0
> offsetY: 0
> offsetZ: 0

# · speed 节点
这个节点代表粒子效果的扩散速度，如果设置得很高，粒子效果会很快扩散  
通常设置为0
> 示例:
> speed: 0

# · range 节点
通常设置为 10

# precision 节点
这个代表你粒子效果的密度(除画圆的粒子效果以外)  

→ 如果粒子效果显示不完全，试着把这个调高  

如果你的服务器卡顿，试着把这个调高(应该不会卡)  
通常设置成0.1~0.01,太小了可能会报错……
> 示例:  
> precision: 0.1

# circlePrecision 节点
这个代表你画圆时粒子效果的密度(360度中每多少度放一个粒子效果)

→ 如果粒子效果显示不完全，试着把这个调高  

如果你的服务器卡顿，试着把这个调高(应该不会卡)  

通常设置成 5
> 示例:  
> circlePrecision: 5



