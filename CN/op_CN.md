[<< 返回中文主页](README_CN.md)
# 运算 (Op)

**运算 (Op)** (即为**operation**的简称) 是一种 (主要) 用于整数/浮点数的变量的运算.
|名称|运算|文本形式|块格式|示例|`c`的值|
|----|--------|-------------------|--------------------|------|-----|
|加法 | `+` | `op add c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839380-4ba4907d-0b36-4402-97b4-6b81e43a65da.png)| `op add c 3 2`| 5|
|减法 | `-` | `op sub c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839396-7b90dd30-c9a6-457e-a67f-4995289d3ee0.png) | `op sub c 3 2`| 1|
|乘法 | `*` | `op mul c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839416-4a44aef5-0aa6-45d2-8997-90d511d10858.png) | `op mul c 2 3` |6|
|除法| `/` | `op div c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839886-fad107d7-044b-4c93-9507-afc215d61d5b.png) | `op div c 5 2` | 2.5|
|整数除法| `//` | `op idiv c a b`| ![image](https://user-images.githubusercontent.com/94273523/154840014-abf42cf2-0ecf-4c5e-af64-7141bae21d54.png) | `op idiv c 5 2`|2|
|模/余数| `%` | `op mod c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840023-4ae73f76-a911-4377-88ea-8a0ca4c6ccdc.png) | `op mod c 5 2` |1|
|指数分布 | `^` | `op pow c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840035-35e69645-e750-41fd-aa78-80bfe84f8348.png) | `op pow c 2 10` |1024|
|相等| `==` | `op equal c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840048-aff01cd8-6809-4a7b-b24e-c4b4b023c57f.png) | `op equal c 2 3`<br>`op equal c 2 2`|0<br>1|
|不相等| `not` | `op notEqual c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840063-a1809838-e8cc-41aa-b167-d04c7548389f.png)|`op notEqual c 2 3`<br>`op notEqual c 2 2`|1<br>0|
|逻辑与| `and` | `op land c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840570-37a7aad1-3bdc-4c93-84ac-57e44f51f48d.png) | `op land c 1 0 `<br>`op land c 2 2`|0<br>1|
|小于| `<` | `op lessThan c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840973-585b6782-5fc8-4803-a20e-00cf01c34f10.png)| `op lessThan c 4 3`<br>`op lessThan c 2 3`|0<br>1|
|小于或等于| `<=` | `op lessThanEq c a b` | ![image](https://user-images.githubusercontent.com/94273523/154879553-52646911-75ca-44f5-aaa2-e66326441e1e.png)|`op lessThanEq c 4 3`<br>`op lessThanEq c 3 3`|0<br>1|
|大于 | `>` | `op greaterThan c a b` | ![image](https://user-images.githubusercontent.com/94273523/154879929-8fcac898-ed32-4bc2-9927-7a5e6798cfdc.png) |`op greaterThan c 2 3`<br>`op greaterThan c 4 3`|0<br>1|
|大于或等于 | `>=` | `op greaterThanEq c a b` | ![image](https://user-images.githubusercontent.com/94273523/154880203-875c9c13-f533-4b87-9567-309ef372ff1b.png)|`op greaterThanEq c 2 3`<br>`op greaterThanEq c 3 3`|0<br>1|
|严格相等 | `===` | `op strictEqual c a b`| ![image](https://user-images.githubusercontent.com/94273523/154880583-118e117b-289e-4920-b28e-ade70b26a74a.png)|`op strictEqual c 1 true`<br>`op strictEqual c 1 1`|0<br>1|

## 二进制运算 (Binary operations)

### 什么是二进制
简单地说, 它是计算机用来表示数字的数字系统. 人类使用十进制(base10)数字系统, 它有唯一的10位数字(0, 1, ....0).

计算机使用二进制(ase2)数字系统, 只有两位数字: 0和1.

### 二进制到十进制转换: 
以'101101'为例, 转换如下: 

<img height=400 src="https://user-images.githubusercontent.com/94273523/154889433-1d810ffa-5675-4508-ab24-4516d732ab3a.png" />
来源: https://www.cuemath.com/numbers/binary-to-decimal/

### 十进制到二进制的转换
以'13'为例, 转换如下: 

<img height=400 src="https://user-images.githubusercontent.com/94273523/154890032-b8ae8ecf-0d95-4c53-84c1-a0ee6140950e.png" />

来源: https://www.cuemath.com/numbers/decimal-to-binary/

在我向你们展示操纵数字位的运算器之前，你们需要知道它们的简单版本，即

在2bits上运行：

### '或' (or)
如果其中一个参数为1, 则计算为1, 否则为0. 这可能是

以更紧凑的形式表示, 称为[真值表](https://en.wikipedia.org/wiki/Truth_table)

```
| or | 1 | 0 |
| 1  | 1 | 1 |
| 0  | 1 | 0 |
```
意为:
* 1 `or` 1 is 1
* 1 `or` 0 is 1
* 0 `or` 1 is 1
* 0 `or` 0 is 0

### '和' (and)
如果**所有**的参数为1, 则计算为1, 否则为0.
 ```
| and | 1 | 0 |
|  1  | 1 | 0 |
|  0  | 0 | 0 |
```

### '不相等' (not)
反转它的参数: 0变为1, 反之亦然.

### '按位异或' (xor)
如果1**且其参数中只有**1为1, 则计算为1, 否则为0.
 ```
| xor | 1 | 0 |
|  1  | 0 | 1 |
|  0  | 1 | 0 |
```

一旦你了解了这些, 就应该了解: 

### 位操作符（Bitwise operators）

它会基于它的一些参数进行操作, 这些参数通常由上面描述的简单运算符组成.

|名称|运算|示例|`c`的值|解释|
|----|--------|------|------------|-----------|
|左位移 | `<<` | `op shl c 2 4` |32|将2('00000010')的位向左移动4位(并将其存储在`c`中):<br>`00000010`<br>变为<br>`00100000`|
|右位移| `>>` | `op shr c 32 4`|2|将32('00100000')的位向右移动4位(并将其存储在`c`):<br>`00100000`<br>变为<br>`00000010`|




`op`会接受1或2个参数, 并将结果写入变量. 例子
```
set a 1
set b 2
op add c a b
print c
printflush message1
```
这将使'a'和'b'相加, 并将结果存储在'c'中, 然后将其打印到信息板中.

[^1] 需要进一步讨论
