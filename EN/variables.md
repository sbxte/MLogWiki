[<< return to main page](../README.md)
# Variables

Variables, almost any information in mindustry can be stored in them.
Just like other programming languages, they are the core of mlog.


## Data Types

- Integers/Floats
- Booleans
- String literals
- Units
- Unit Types
- Buildings
- Building Types
- Sensables (Used in sensor)
- Tile Type

Sensoring only works entities.

## Set and Operation

By default any variable has nothing (`null`) stored in them.
- `set` is an instruction used to set a variable's contents. *[Read further about set](set.md)*
- `op` is an instruction used to perform an operation on a variable's contents. `op` is mainly used for mathematical operations on integer/float type variables, but can "work" on others due to coercion. *[Read further about op](op.md)*

## Coercion

*Not written yet*

## Unlisted variables

These variables cannot be found in the sensor instruction nor the core database.

Processor specific:
- `@counter` - The index of the instruction currently being executed by the processor. This index starts from 0, ie the first instruction is at 0, not at 1.
- `@unit` - The processor's currently binded unit.
- `@thisx` - The processor's x coordinate. Whole numbers for odd width processors and fractional for even widths.
- `@thisy` - The processor's y coordinate. Whole numbers for odd width processors and fractional for even widths.
- `@ipt` - The processor's instruction per tick speed. Its 2 for a microprocessor, 8 for a logic processor, and 25 for a hyperprocessor.
- `@links` - The amount of buildings linked to a processor. This is often used to iterate through buildings with `getlink`

Time (same for all processors across the map):
- `@time` - The amount of microseconds from when the save was loaded/game started.
- `@ticks` - The amount of ticks from when the save was loaded/game started.

Map specific:
- `@maph` - The map's height.
- `@mapw` - The map's width.

Tile type (these can be checked against tiles stored in vars using `jump`)
- `@air` - The tile is air and can be built/walked on.
- `@solid` - The tile is a solid (eg walls, terrain) and cannot be built or walked on.

Command center config:
- `@commandAttack`
- `@commandRally`
- `@commandIdle`
