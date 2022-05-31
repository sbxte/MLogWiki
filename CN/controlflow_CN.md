[<< 返回中文主页](README_CN.md)
# 控制流 (Control Flow)

控制流是正在执行的指令的顺序.
处理器按照从最上面的指令到最下面的指令的顺序执行代码.
当它最后一个指令执行完毕时, 它会自动循环回到最开始的指令.

## 跳转 (Jumps)

跳转指令可用于直接跳转/跳过到特定指令. *(有关跳转标签的更多信息, 请查看[编辑](editing_CN.md))*
举个例子,
```
print "你好!\n"
jump goHere always 0
    print "这条不会被打印出来!"
goHere:
print "这条会被打印出来!"
printflush message1
```
![QQ浏览器截图20220526174029](https://user-images.githubusercontent.com/63439268/170462900-7ee04e52-7295-4595-8897-b71db51be33b.png)

跳转有8个运算符 *([请查看运算部分](op_CN.md))*:
- `==` 相等
- `!=` 不相等
- `===` 绝对相等
- `>` 大于
- `<` 小于
- `>=` 大于或等于
- `<=` 小于或等于
- `always` 无论条件如何, 总是跳转
- 
### 条件判断 (If-else)

一个条件判断语句的例子
```
set a 3
jump else notEqual a 3
    print "A是3"
    jump end_if_else always 0
else:
    print "A不是3"
end_if_else:
printflush message1
```
![QQ浏览器截图20220526174043](https://user-images.githubusercontent.com/63439268/170462936-fed5116c-080e-4f17-919b-1cbe8cafc768.png)

## 结束 (End)

总是跳转至0还有一个更容易使用的对应项, `end`.
`end`与'jump 0 always'完全相同, 只是它没有跳转箭头.
这可以减少跳转箭头导致的代码混乱, 或者仅是让代码更易查看.

```
printflush message1
print "这条会被打印出来"
jump 0 always
print "这条不会"
```
等同于
```
printflush message1
print "这条会被打印出来"
end
print "这条不会"
```
![QQ浏览器截图20220526174056](https://user-images.githubusercontent.com/63439268/170462998-c519039a-96dd-4487-8527-02b3ce40c07e.png)

## 等待 (Wait)

等待指令用于在执行下条指令之前暂停执行等待一段时间.
这是一个每秒都在变换颜色的彩色文本,
```
print "[red]你好!"
printflush message1
wait 1
print "[yellow]你好!"
printflush message1
wait 1
print "[green]你好!"
printflush message1
wait 1
print "[blue]你好!"
printflush message1
wait 1
```
![image](https://user-images.githubusercontent.com/63439268/157013612-706ddb9d-297f-4b4a-a16d-902cc7558361.gif)

## @counter

没有多少人知道这个功能, 但`@counter`可以被指令**修改** *(查看[赋值](set_CN.md) 和[运算](op_CN.md))*.
```
print "这条会被打印出来"
set @counter 3
print "这条不会"
printflush message1
```
![QQ浏览器截图20220526174056](https://user-images.githubusercontent.com/63439268/170462998-c519039a-96dd-4487-8527-02b3ce40c07e.png)

在本示例中, 我们将`@counter`的值设为3后, 会跳过第二条`print`指令直接执行`printflush`指令.

它还可以用于跳转到不同的位置以创建一个数组.
```
op mul counterJump index 2
op add @counter @counter counterJump
    set x 0
    jump jumpEnd always 0
    set x 1
    jump jumpEnd always 0
    set x 2
    jump jumpEnd always 0
    set x 3
jumpEnd:
print x
printflush message1
op add index index 1
op mod index index 4
```
![image](https://user-images.githubusercontent.com/63439268/157013753-66d43a58-833f-43a2-8053-7c843f741866.gif)
