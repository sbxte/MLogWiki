[<< return to main page](../README.md)
# Editing code

> Taken from the official wiki

There are two primary methods to writing Mindustry Logic: The Visual Editor and manual editing. Each is better in their own way, so choose whichever works for you the best.

## The Visual Editor

The Visual Editor is the "Editing" interface of a processor (when you press the "pencil" button). It's the recommended method for beginners, since it has been designed to be easy to understand and use.

The advantages of editing this way as opposed to editing manually are:

- A block-based, color-coded, drag-and-drop interface
- Easy parameter chooser, shows all of the needed parameters
- Visual, easy-to-set jump relationships
- Mobile-friendly

![image](https://mindustrygame.github.io/wiki/images/misc/logic-editing-visualEditor-overview.png)

You can also export and import code to and from text form.

## Manual Editing

Manual editing involves using a text editor such as Notepad++, Vim, or Visual Studio Code to edit your code. For more advanced users and longer code, manual editing is the way to go.

The advantages of manually editing code as opposed to the Visual Editor are:

- Denser than the Visual Editor; more code can be seen at a time
- Typing is faster than dragging-and-dropping across long walls of code
- Can be used to make quick pieces of code for demonstration without opening Mindustry
- Syntax highlighting in some editors, such as VS Code (plugin), Emacs (package), Vim (plugin), and Sublime Text (package)
- A text block does not block part of the parameter text
- Ability to save and access code outside of Mindustry
- Comments, indentation and jump labelling, to help keep track of loops and functions in longer codes.

However, it can be a little difficult for beginners or those who aren't used to editing code.

### Comments

Comments can be used to explain what the code does, and to help keep track of the code. Comments aren't preserved nor are they viewable in the visual editor.
```
# Set a = 1, b = 2, c = 4
set a 1
set b 2 # On this line, b is set to 2
set c 4
#This is a comment, they start with "#"s
jump jumpHere equal a 1 # Jump if a is equal to 1
    set d 0
    end
jumpHere:
set d 3
```

### Jump labels

Jump labels can be used on `jump` instructions when manually editing.
They can help denote functions and loops like comments do.
```
set a 0
loop:
    op add a a 1
jump loop lessThan a 5 # Keep adding a until its 5, then reset a to 0
```

### Indentation and spacing

When manually editing code, you can use indentation and spacing between instructions to help prettify or make your code more readable.
These spaces will disappear when you paste them into the visual editor.
```
set a 1

# Woah thats some spacing between instructions
set b 2


# and even more spacing!


set c 4

set d 0
loop:
            print "You can also add as many indents as you want"
                                print "\nAlthough I would advise you not to abuse it :)"
    op add d d 1
jump loop lessThan d 3

# Now we flush it into a message block
    printflush message1
```
