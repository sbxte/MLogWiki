[<< return to main page](../README.md)
[<< return to main page](../README.md)
# Print

`print` and `printflush` are the 2 instructions you use to display text unto a linked message block.
Doing `print` holds the text until `printflush` is performed on a linked message block.

You can print strings,
```
print "Hello World!"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833019-9249388a-a101-4f6d-81c1-0485b89c18be.png)

and variables
```
set a 10
print a
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833028-2ac9e0c4-9a69-4a6f-8dde-c2799625a414.png)


You can also chain multiple prints before flushing it into a message block.
```
print "A "
print "B "
print "C "
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833040-5bf0c473-00b4-4ea2-ac90-680cad2e9115.png)


To print a new line, use the escape sequence `\n`
```
print "This is a line"
print "\nThis is another line"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833051-ba869cf0-043f-450f-81ac-57f3a46153d6.png)

```
print "This is line 1\nAnd this is line 2"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833120-50b93082-fd54-4de5-9ef4-38e8ebca21fa.png)


However, there are limits to how much you can have printed into a message block. *The internal values can be found [here](https://github.com/Anuken/Mindustry/blob/master/core/src/mindustry/world/blocks/logic/MessageBlock.java#L23)*

- Maximum characters: 200
- Maximum lines: 24

You can test it out yourself with a bunch of newlines
```
print "0\n1\n2\n3\n4\n5\n6\n7\n8\n9\n10\n11\n12\n13\n14\n15\n16\n17\n18\n19\n20\n21\n23\n24\n25\n26\n27\n28"
printflush message1
```
![image](https://user-images.githubusercontent.com/94273523/154833097-0b4a2f8f-a566-46bc-b426-bf213141888e.png)

Notice how the lines cut off at 24. The same thing applies for characters, except the limit is 200 instead of 24.
