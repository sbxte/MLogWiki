# Print

`print`和`printflush`是用于使被链接的信息板显示文本的2条指令.
在链接的存储单元上执行`printflush`之前, 执行`print`会一直保存文本.

你可以打印字符串(strings),
```
print "你好世界!"
printflush message1
```
和变量(variables)
```
set a 10
print a
printflush message1
```

你还可以在多个打印内容打印到信息板之前将其链接起来.
```
print "A "
print "B "
print "C "
printflush message1
```

要想另起一行, 请使用特殊字符 `\n`
```
print "这是一行"
print "\n这是另一行"
printflush message1
```
```
print "这是行1\n这是行2"
printflush message1
```

然而, 你可以打印到信息板的内容是有上限的. *内部值可在[这里](https://github.com/Anuken/Mindustry/blob/master/core/src/mindustry/world/blocks/logic/MessageBlock.java#L23)找到*

- 最大字符: 200
- 最大行数: 24

亦可以用一堆新行测试一下
```
print "0\n1\n2\n3\n4\n5\n6\n7\n8\n9\n10\n11\n12\n13\n14\n15\n16\n17\n18\n19\n20\n21\n23\n24\n25\n26\n27\n28"
printflush message1
```
请注意这些新行是如何在第24行断开的. 该效果同样适用于字符, 但字符的上限是200而非24.
