[<< 返回中文主页](README_CN.md)
# 获取连接 (Getlink)

`getlink`是做什么的?
基本上, 当你使用处理器连接建筑时 (例如. message1, cell1, reactor1 等等),
它会根据连接的顺序获取一个数字.
因此, 如果你先连接一个信息板然后再连接内存元, 执行 getlink 0 将会等同于在 message1 上执行, 并且 getlink 1 将会等同于在 cell1 上执行.

*请注意, 获取连接的默认索引为0, 从0开始计数, 而不是从1开始.*

如果你需要在许多不同的方块上执行相同的代码, 这将非常有用, 例如一个钍反防爆装置:
```
getlink reactor i
sensor cryofluid reactor @cryofluid
op greaterThan boolean cryofluid 8
control enabled reactor boolean 0 0 0
op add i i 1
op mod i i @links
```
这将遍历所有被连接的方块, 并禁用任何缺少冷冻液的方块.

> [摘自highfire在Mindustry Discord上的解释](https://discord.com/channels/391020510269669376/742769933926269069/867577676059115520)

## @links

`@links`只是处理器连接的建筑的数量,
`@links`的索引不是0, 它们从1开始计数, 而不是从0开始.
这对于遍历建筑很有用 (就像上面的例子一样).
