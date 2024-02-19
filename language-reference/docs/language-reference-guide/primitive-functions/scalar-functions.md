# Scalar Functions

There is a class of primitive functions termed scalar functions This class is identified in [Table 1](#ScalarPrimitiveFunctions) below. Scalar functions are **pervasive**, i.e. their properties apply at all levels of nesting.  Scalar functions have the following properties:

Scalar Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `+` | [Conjugate](Conjugate.htm) | [Plus (Add)](Add.htm) |
| `-` | [Negative](Negative.htm) | [Minus (Subtract)](Subtract.htm) |
| `×` | [Direction (Signum)](Direction.htm) | [Times (Multiply)](Multiply.htm) |
| `÷` | [Reciproca](Reciprocal.htm) l | [Divide](Divide.htm) |
| `|` | [Magnitude](Magnitude.htm) | [Residue](Residue.htm) |
| `⌊` | [Floor](Floor.htm) | [Minimum](Minimum.htm) |
| `⌈` | [Ceiling](Ceiling.htm) | [Maximum](Maximum.htm) |
| `*` | [Exponential](Exponential.htm) | [Power](Power.htm) |
| `⍟` | [Natural Logarithm](Natural Logarithm.htm) | [Logarithm](Logarithm.htm) |
| `○` | [Pi Times](Pi Times.htm) | [Circular](Circular.htm) |
| `!` | [Factorial](Factorial.htm) | [Binomial](Binomial.htm) |
| `~` | [Not](Not.htm) | $ |
| `?` | [Roll](Roll.htm) | $ |
| `∊` | [Type](Type.htm) (See [Enlist](Enlist.htm) ) | $ |
| `^` |  | [And](And Lowest Common Multiple.htm) |
| `∨` |  | [Or](Or Greatest Common Divisor.htm) |
| `⍲` |  | [Nand](Nand.htm) |
| `⍱` |  | [Nor](Nor.htm) |
| `<` |  | [Less](Less.htm) |
| `≤` |  | [Less Or Equal](Less Or Equal.htm) |
| `=` |  | [Equal](Equal.htm) |
| `≥` |  | [Greater Or Equal](Greater Or Equal.htm) |
| `>` |  | [Greater](Greater.htm) |
| `≠` |  | [Not Equal](Not Equal.htm) |
| $ Dyadic form is not scalar | $ Dyadic form is not scalar | $ Dyadic form is not scalar |

### Monadic Scalar Functions

- The function is applied independently to each simple scalar in its argument.
- The function produces a result with a structure identical to its argument.
- When applied to an empty argument, the function produces an empty result.  With the exception of `+` and `∊`, the type of this result depends on the function, not on the type of the argument. By definition + and `∊` return a result of the same type as their arguments.
### Example
```apl
      ÷2 (1 4)
0.5  1 0.25
```

### Dyadic Scalar Functions

- The function is applied independently to corresponding pairs of simple scalars in its arguments.
- A simple scalar will be replicated to conform to the structure of the other argument.  If a simple scalar in the structure of an argument corresponds to a non-simple scalar in the other argument, then the function is applied between the simple scalar and the items of the non-simple scalar.  Replication of simple scalars is called scalar extension.
- A simple unit is treated as a scalar for scalar extension purposes.  A unit is a single element array of any rank.  If both arguments are simple units, the argument with lower rank is extended.
- The function produces a result with a structure identical to that of its arguments (after scalar extensions).
- If applied between empty arguments, the function produces a composite structure resulting from any scalar extensions, with type appropriate to the particular function. (All scalar dyadic functions return a result of numeric type.)

### Examples
```apl
      2 3 4 + 1 2 3
3 5 7
 
      2 (3 4) + 1 (2 3)
3  5 7
 
      (1 2) 3 + 4 (5 6)
 5 6  8 9

      10 × 2 (3 4)
20  30 40
 
      2 4 = 2 (4 6)
1  1 0

      (1 1⍴5) - 1 (2 3)
4  3 2

      1↑''+⍳0
0
       1↑(0⍴⊂' ' (0 0))×''
0  0 0
```

**Note:**  The Axis operator applies to all scalar dyadic functions.
