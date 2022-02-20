[<< return to main page](../README.md)
# Print

`print` and `printflush` are the 2 instructions you use to display text unto a linked message block.
Doing `print` holds the text until `printflush` is performed on a linked message block.

You can print strings,
```
print "Hello World!"
printflush message1
```
and variables
```
set a 10
print a
printflush message1
```

You can also chain multiple prints before flushing it into a message block.
```
print "A "
print "B "
print "C "
printflush message1
```

To print a new line, use the special character `\n`
```
print "This is a line"
print "\nThis is another line"
printflush message1
```
```
print "This is line 1\nAnd this is line 2"
printflush message1
```

However, there are limits to how much you can have printed into a message block. *The internal values can be found [here](https://github.com/Anuken/Mindustry/blob/master/core/src/mindustry/world/blocks/logic/MessageBlock.java#L23)*

- Maximum Characters: 200
- Maximum Newlines: 24

You can test it out yourself with a bunch of newlines
```
print "0\n1\n2\n3\n4\n5\n6\n7\n8\n9\n10\n11\n12\n13\n14\n15\n16\n17\n18\n19\n20\n21\n23\n24\n25\n26\n27\n28"
printflush message1
```
Notice how the lines cut off at 24. The same thing applies for characters, except the limit is 200 instead of 24.
