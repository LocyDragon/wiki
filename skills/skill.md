# 技能组(Skills)
# 示例技能组
>示例技能组可以在  
./plugins/RevivedLocyItem/Skills/ExampleSkills.yml查看，建议配合示例技能组来阅读wiki!  
>注意节点大小写
>
>请确保你已经阅读完 [Item物品] 相关内容!

# · cooldown 节点
这个节点可以填写一个数字，代表该技能组的冷却时间(秒为单位)

# · wait 节点
当技能组还在冷却时间时，会发送这条信息!  
其中变量 {cd} 代表剩余冷却时间的秒数!  

# · condition 节点
这个节点下面可以写一些执行该技能组的条件

条件的格式为
> [条件名] ~ value=[条件值];fail=[判断失败发送的信息，可以不填，不填就不发送]


## · 条件类型：random
这个条件，代表该技能组的执行概率(0-1)

> value = 概率 
>
> 例子:  
>
> random ~ value=0.75;fail=&c这个技能只有75%的概率被执行哦~

## · 条件类型：permission/perm
这个条件，代表判断玩家是否有权限使用某个技能

> value = 权限名称
>
> 例子:  
>
> permission ~ value=MyItem.use;fail=&c你没有权限使用这个物品

## · 条件类型：compare
这个条件，代表比较（数据/字符串）

> value = 比较类型
>
> 关于比较类型，可以写
>
>
> ①数值比较(>、<、=)
>
> 如:  1>0、5*5>2、%player_level%<20、%player_level%*2=8
>
> ②字符串比较(equals)，自动忽略大小写
>
> 如：%player_name% equals FuzhuDada
>
> 例子:  
>
> compare ~ value=%player_level% > 9;fail=只有十级和以上才能用呢.
>
> compare ~ value=%player_name% equals FuzhuDada;fail=只有FuzhuDada可以使用！

# · Skills 节点
这个地方，你可以书写一些技能。与Item(物品)里面的Skills不同的地方是，  
你不需要添加触发条件，其余都和Item里的Skills用法相同    
而且你可以使用delay参数来控制单个技能与技能之间的空闲时长   

delay 参数的用法:  
delay ~ 毫秒(1秒=1000毫秒)

例子:
>   msg ~ m=&7Chug! Chug! #发送信息    
    particle ~ name=Star #执行粒子效果组    
    lightning  #雷电   
    delay ~ 1000 #间隔一秒    
    launch ~ type=FireBall;d=15 #发射火球    
    push ~ dp=-1.6;dh=0.8 #把玩家向后推动  
  
