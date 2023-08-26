# 粒子效果组(Particles)
# 示例粒子效果组
>示例效果组可以在  
./plugins/RevivedLocyItem/Particles/ExampleParticle.yml查看，建议配合示例粒子效果组来阅读wiki!  
>注意节点大小写
>
>请确保你已经阅读完 [Skills技能组] 相关内容!  

粒子效果组是什么？  
这个东西，可以让你在一个空间"直角坐标系"中画出一些粒子效果组，支持延迟  

## ! 粒子效果种类对应的英文名

注：只有部分粒子效果：如REDSTONE，后面可以添加color参数修改其RGB颜色，如
> line ~ A=(2,0,2);B=(-2,0,-2);type=REDSTONE;color=#800080

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

# · head 节点
当设置为true时，粒子效果的位置会根据你的头的角度而改变

这个节点代表头坐标系是否开启，选择true/false
> 示例:  
> head: true

# · rotate 节点
这个节点有四个参数，依次为：角度(弧度制),旋转向量轴x,旋转向量轴y,旋转向量轴z

注意角度是弧度制而非角度制，二者的换算为：弧度制=角度*π/180

比如45°对应的弧度为π/4，大约为0.75

后面三个参数为旋转轴，这三个参数代表一个旋转轴向量的(x,y,z)，整个图像会绕着这个向量进行一次一定角度的旋转，以该向量为轴！

举一个例子，如果你写一个(0,1,0)来进行旋转，并且旋转的目标图形是玩家脚下的一个圆，那么转了跟没转没啥区别

这是因为0,1,0是一个竖着的向量，而圆是完全对称图形，原地转了一下等于没转
> 示例:  
> rotate: (0.75,1,0,0)

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

# · precision 节点
这个代表你粒子效果的密度(除画圆的粒子效果以外)  

→ 如果粒子效果显示不完全，试着把这个调高  

如果你的服务器卡顿，试着把这个调高(应该不会卡)  
通常设置成0.1~0.01,太小了可能会报错……
> 示例:  
> precision: 0.1

# · circlePrecision 节点
这个代表你画圆时粒子效果的密度(360度中每多少度放一个粒子效果)

→ 如果粒子效果显示不完全，试着把这个调高  

如果你的服务器卡顿，试着把这个调高(应该不会卡)  

通常设置成 5
> 示例:  
> circlePrecision: 5

# · Effect 节点
这个节点下，用于编写一些粒子效果组。可以使用延迟  
书写格式:
> 形状名称 ~ 值名1=xxx;值名2=xxx;值名3=xxx;type=粒子效果名称  
> 其中,type代表了执行这个形状时，使用的粒子效果种类，比如说你要画一个绿色的圆  
> type可以填写HAPPY_VILLAGER!

## 流程名称 —— delay
作用:延迟执行  
书写格式:  
> delay ~ 毫秒数(1秒=1000毫秒)

## 形状名称 —— line
使用这个形状，可以画出一条线段
首先，你要在坐标系中选取两个点，记作A(x1,y1,z1);B(x2,y2,z2)，填写参数即可
> 书写格式:  
> line ~ A=(x1,y1,z1);B=(x2,y2,z2);type=粒子效果种类(见上面)  
>
> 其中，A和B是该线段的两个端点  
> 
> 例子:
> line ~ A=(2,0,2);B=(-2,0,-2);type=REDSTONE;color=#800080
>
> 在(2,0,2)到(-2,0,-2)之间画一条线，线的红色为紫色(color)

## 形状名称 —— circle
使用这个形状，可以画出一个圆  
首先，你要在坐标系中找出一个圆心坐标，并确定它的半径!  
> 书写格式:
> circle ~ centre=(x1,y1,z1);r=半径;粒子效果种类(见上面)  
>
> 其中，centre是圆心的坐标  
> 
> 例子:
> circle ~ centre=(0,0,0);r=2.82842;type=SMOKE  
>
> 以(0,0,0为圆心)，2.82842(约为2√2)为半径画圆，材质为SMOKE  

## 形状名称 —— f
使用这个形状，可以画出一个函数的图像  
首先，你要确定函数的表达式和它的值域!  
> 书写格式:  
> f ~ start=开始x坐标;end=终止x坐标;ex=函数表达式;symmetric=是否关于原点旋转90°;type=粒子效果种类(见上面)  
> 注意: start < end  
> 注意: symmetric填写true就是旋转90°，false就是不旋转!  
> 注意: ex只要填写一个关于x的式子就行了  
>
> 例子:  
> f ~ start=-2;end=2;ex=x*x+0.5;symmetric=true;type=HAPPY_VILLAGER
>
> 这样子就画出了y=x^2+0.5的图像从-2到2的部分，并且关于原点旋转90°的图像，图像的  
> 材质是HAPPY_VILLAGER(一种绿色的粒子效果)



