[<< return to main page](../README.md)
# Unit Bind

The Unit Bind (or ubind for short) instruction is the gateway to unit logic, as the other unit commands are useless without it.
It has only one parameter, in which you input the unit type you want to bind.
When ubind is executed, it binds only 1 unit, and the reference to that bound unit is saved to @unit.

A few things to keep in mind:
- You can save a bound unit's reference to a variable. Example:
```
ubind @flare
set unit_reference @unit
```
`unit_reference` is the variable that contains the reference to the bound unit.

![image](https://user-images.githubusercontent.com/63439268/157014208-67a6e59a-10c6-436e-8183-4c2e4da09ed9.png)

- You can bind a specific by inputting it's reference into the ubind instruction. Example:
```
ubind unit_reference
```
Where `unit_reference` is the previously saved unit.
- Inputting anything other than a unit type or unit reference will set @unit to null.
- You can't bind units from other teams.
- You can bind core units! but you can't run any unit instruction on them, though other instructions like `sensor` would still work.
- `@unit`, as well as other saved references will be wiped out after map reload. So be careful.
- You can't bind multiple units at the same time, as they will overwrite each other.
- Binding a unit doesn't mark it as controlled (`@controlled`)
