[<< return to main page](../README.md)
# Control Flow

Control flow is the order of instructions being executed.
Processors execute code in order from the top most instruction to the bottom most.
When it finishes executing the last instruction, it loops back to the start automatically.

## Jumps

Jumps can be used to jump/skip straight to a specific instruction. *(checkout [editing](editing.md) for more on jump labels)*
For example,
```
print "Hello!\n"
jump goHere always 0
    print "This will not be printed!"
goHere:
print "This will be printed!"
printflush message1
```

Jumps have 8 operators *([check out the op section](op.md))*:
- `==` equality
- `!=` inequality
- `===` strict equality
- `>` greater than
- `<` less than
- `>=` greater than or equal to
- `<=` less than or equal to
- `always` always jumps regardless of conditions

### If-else

An example of if-else statements
```
set a 3
jump else notEqual a 3
    print "A is 3"
    jump end_if_else always 0
else:
    print "A is not 3"
end_if_else:

printflush message1
```

## End

Jumping always to 0 also has an easier to use counterpart, `end`.
`end` is exactly the same as `jump 0 always` with the exception of it losing its jump arrow.
This can reduce clutter in code from jump arrows or just make it easier to look at.

```
printflush message1
print "This will be printed"
jump 0 always
print "This will not"
```
Is the same as
```
printflush message1
print "This will be printed"
end
print "This will not"
```

## Wait

The wait instruction is used to pause execution for a period of time before continuing to the next instruction.
Here is a colored text changing every second,
```
print "[red]Hello!"
printflush message1
wait 1
print "[yellow]Hello!"
printflush message1
wait 1
print "[green]Hello!"
printflush message1
wait 1
print "[blue]Hello!"
printflush message1
wait 1
```

## @counter

Not many know of this feature, but `@counter` can be **modified** with instructions *(check out [set](set.md) and [operation](op.md))*.
```
print "This will be printed"
set @counter 3
print "This will not"
printflush message1
```
In this example, we set `@counter` to 3 which is the `printflush` instruction, skipping the 2nd `print` instruction.

It can also be used to jump to different locations to create an array.
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
