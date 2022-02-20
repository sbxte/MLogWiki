# Op

**Op** (or short for **operation**) is used (mainly) on integer/float variables to perform calculations.
The operation types which can be done are:
- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Exponention (^)
- Modulo (%)
- Floor division (idiv)
- Sine (sin)
- Cosine (cos)
- Tangent (tan)
- Logarithm (log)
- Natural logarithm (ln)
- 2D Noise (noise)

`op` takes in 1 or 2 arguments and writes the outcome into a variable. Example,
```
set a 1
set b 2
op add c a b
print c
printflush message1
```
This will add `a` and `b` and store the result in `c` which is then printed into a message block.
