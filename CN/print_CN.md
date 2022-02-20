[<< 返回中文主页](CN/README_CN.md)
# 打印 (Print)

`print`和`printflush`是用于使被链接的信息板显示文本的2条指令.
在被连接的信息板上执行`printflush`之前, 执行`print`会一直保存文本.

你可以打印字符串(strings),
```
print "你好世界!"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833019-9249388a-a101-4f6d-81c1-0485b89c18be.png)

和变量(variables)
```
set a 10
print a
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833028-2ac9e0c4-9a69-4a6f-8dde-c2799625a414.png)

你还可以在多个打印内容刷新到信息板之前将其链接起来.
```
print "A "
print "B "
print "C "
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833040-5bf0c473-00b4-4ea2-ac90-680cad2e9115.png)

要想另起一行, 请使用转义字符 `\n`
```
print "这是一行"
print "\n这是另一行"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833051-ba869cf0-043f-450f-81ac-57f3a46153d6.png)

```
print "这是行1\n这是行2"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833120-50b93082-fd54-4de5-9ef4-38e8ebca21fa.png)

然而, 你可以打印到信息板的内容是有上限的. *内部值可在[这里](https://github.com/Anuken/Mindustry/blob/master/core/src/mindustry/world/blocks/logic/MessageBlock.java#L23)找到*

- 最大字符: 200
- 最大行数: 24

你可以用一堆新行测试一下
```
print "0\n1\n2\n3\n4\n5\n6\n7\n8\n9\n10\n11\n12\n13\n14\n15\n16\n17\n18\n19\n20\n21\n23\n24\n25\n26\n27\n28"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833097-0b4a2f8f-a566-46bc-b426-bf213141888e.png)

请注意这些新行是如何在第24行隔断的. 该效果同样适用于字符, 但字符的上限是200而非24.
