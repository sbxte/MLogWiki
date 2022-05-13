[<< return to main page](../README.md)
# Op

**Op** (or short for **operation**) is used (mainly) on integer/float variables to perform calculations.
|Name|Operator|Text form|Block form|Examle|Value of `c`|
|----|--------|-------------------|--------------------|------|-----|
|Addition | `+` | `op add c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839380-4ba4907d-0b36-4402-97b4-6b81e43a65da.png)| `op add c 3 2`| 5|
|Subtraction | `-` | `op sub c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839396-7b90dd30-c9a6-457e-a67f-4995289d3ee0.png) | `op sub c 3 2`| 1|
|Multiplication | `*` | `op mul c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839416-4a44aef5-0aa6-45d2-8997-90d511d10858.png) | `op mul c 2 3` |6|
|Division| `/` | `op div c a b` | ![image](https://user-images.githubusercontent.com/94273523/154839886-fad107d7-044b-4c93-9507-afc215d61d5b.png) | `op div c 5 2` | 2.5|
|Integer division| `//` | `op idiv c a b`| ![image](https://user-images.githubusercontent.com/94273523/154840014-abf42cf2-0ecf-4c5e-af64-7141bae21d54.png) | `op idiv c 5 2`|2|
|Modulo/remainder| `%` | `op mod c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840023-4ae73f76-a911-4377-88ea-8a0ca4c6ccdc.png) | `op mod c 5 2` |1|
|Exponential | `^` | `op pow c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840035-35e69645-e750-41fd-aa78-80bfe84f8348.png) | `op pow c 2 10` |1024|
|Equality| `==` | `op equal c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840048-aff01cd8-6809-4a7b-b24e-c4b4b023c57f.png) | `op equal c 2 3`<br>`op equal c 2 2`|0<br>1|
|Inequality| `not` | `op notEqual c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840063-a1809838-e8cc-41aa-b167-d04c7548389f.png)|`op notEqual c 2 3`<br>`op notEqual c 2 2`|1<br>0|
|Bitwise and| `and` | `op land c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840570-37a7aad1-3bdc-4c93-84ac-57e44f51f48d.png) | `op land c 1 0 `<br>`op land c 2 2`|0<br>1|
|Less than| `<` | `op lessThan c a b` | ![image](https://user-images.githubusercontent.com/94273523/154840973-585b6782-5fc8-4803-a20e-00cf01c34f10.png)| `op lessThan c 4 3`<br>`op lessThan c 2 3`|0<br>1|
|Less than or equal to| `<=` | `op lessThanEq c a b` | ![image](https://user-images.githubusercontent.com/94273523/154879553-52646911-75ca-44f5-aaa2-e66326441e1e.png)|`op lessThanEq c 4 3`<br>`op lessThanEq c 3 3`|0<br>1|
|Greater than | `>` | `op greaterThan c a b` | ![image](https://user-images.githubusercontent.com/94273523/154879929-8fcac898-ed32-4bc2-9927-7a5e6798cfdc.png) |`op greaterThan c 2 3`<br>`op greaterThan c 4 3`|0<br>1|
|Greater than or equal to | `>=` | `op greaterThanEq c a b` | ![image](https://user-images.githubusercontent.com/94273523/154880203-875c9c13-f533-4b87-9567-309ef372ff1b.png)|`op greaterThanEq c 2 3`<br>`op greaterThanEq c 3 3`|0<br>1|
|Strict equality | `===` | `op strictEqual c a b`| ![image](https://user-images.githubusercontent.com/94273523/154880583-118e117b-289e-4920-b28e-ade70b26a74a.png)|`op strictEqual c 1 true`<br>`op strictEqual c 1 1`|0<br>1|

## Binary operations

### What is binary
Simply put, it's a number system used by computer to represent number. Human use decimal (base10) number system, which have unique 10 digits (0, 1, ... 0).
Computer use binary (base2) number system which only have 2 digits: 0 and 1.

### Binary to decimal conversion:
Take `101101` as an example, the conversion is as follow:

<img height=400 src="https://user-images.githubusercontent.com/94273523/154889433-1d810ffa-5675-4508-ab24-4516d732ab3a.png" />
source: https://www.cuemath.com/numbers/binary-to-decimal/

### Decimal to binary conversion
Take `13` as an example, the conversion is as follow:

<img height=400 src="https://user-images.githubusercontent.com/94273523/154890032-b8ae8ecf-0d95-4c53-84c1-a0ee6140950e.png" />

source: https://www.cuemath.com/numbers/decimal-to-binary/

Before I show you the oprerators that manipulates bits of a number, you need to know the simple version of them, which
operates on 2 bits:

### `or`
Evaluates to 1 if either one of it's arguments is 1, 0 otherwise. This can be
represented in a more compact form called [truth table](https://en.wikipedia.org/wiki/Truth_table)

```
| or | 1 | 0 |
| 1  | 1 | 1 |
| 0  | 1 | 0 |
```
It means:
* 1 `or` 1 is 1
* 1 `or` 0 is 1
* 0 `or` 1 is 1
* 0 `or` 0 is 0

### `and`
Evaluates to 1 if **all** of it's arguments is 1, 0 otherwise.
 ```
| and | 1 | 0 |
|  1  | 1 | 0 |
|  0  | 0 | 0 |
```

### `not`
Invert it's argument: 0 becomes 1 and vice versa.

### `xor`
Evaluates to 1 if 1 **and only** 1 of it's arguments is 1, 0 otherwise.
 ```
| xor | 1 | 0 |
|  1  | 0 | 1 |
|  0  | 1 | 0 |
```

Once you understand all of those, it's time to learn about:

### Bitwise operators

Which operates on bits of its arguments, often made up of the simple operators described above.

|Name|Operator|Examle|Value of `c`|Explanation|
|----|--------|------|------------|-----------|
|Shift left | `<<` | `op shl c 2 4` |32|Shift the bits of 2 (`00000010`) to the left by 4 places (and store it in `c`):<br>`00000010`<br>becomes<br>`00100000`|
|Shift right| `>>` | `op shr c 32 4`|2|Shift the bits of 32 (`00100000`) to the right by 4 places (and store it in `c`):<br>`00100000`<br>becomes<br>`00000010`|




`op` takes in 1 or 2 arguments and writes the outcome into a variable. Example,
```
set a 1
set b 2
op add c a b
print c
printflush message1
```
This will add `a` and `b` and store the result in `c` which is then printed into a message block.

[^1] Need futher discussion
