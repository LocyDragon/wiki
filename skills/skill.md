# 技能组(Skills)
# 示例技能组
>示例物品可以在  
./plugins/RevivedLocyItem/Items/ExampleSkills.yml查看，建议配合示例技能组来阅读wiki!  
>注意节点大小写
>
>请确保你已经阅读完 [Item物品] 相关内容!

# · cooldown 节点
这个节点可以填写一个数字，代表该技能组的冷却时间(秒为单位)

# · wait 节点
当技能组还在冷却时间时，会发送这条信息!  
其中变量 {cd} 代表剩余冷却时间的秒数!  

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
  