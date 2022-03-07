[<< return to main page](../README.md)
# Getlink

What does `getlink` do?
basically, when you add a link to a processor (e.g. message1, cell1, reactor1, etc),
it gets a number based on the order it was connected to.
Therefore if you connect a message and then a cell, doing getlink 0  will be the same as message1, and getlink 1 will be the same as cell1

*Note that getlink is zero indexed and starts counting from 0, not 1.*

This is super useful if your code needs to run the same code on many different blocks, e.g. an anti-nuke explosion thingamajig:
```
getlink reactor i
sensor cryofluid reactor @cryofluid
op greaterThan boolean cryofluid 8
control enabled reactor boolean 0 0 0
op add i i 1
op mod i i @links
```
![image](https://user-images.githubusercontent.com/63439268/157014517-8afc8e04-0782-4252-a1e2-6e321aaa4a2c.png)

This iterates through all connected blocks and disables any that are lacking cryofluid.

> [Taken from highfire's explanation on the mindustry discord](https://discord.com/channels/391020510269669376/742769933926269069/867577676059115520)


## @links

`@links` is simply the number of buildings that are linked to the processor,
`@links` are not 0 indexed, they start counting from 1, not 0.
This can be useful for iterating through buildings (like in the example shown above).
