# Scalar Functions

There is a class of primitive functions termed scalar functions This class is identified in [Table 1](#ScalarPrimitiveFunctions) below. Scalar functions are **pervasive**, i.e. their properties apply at all levels of nesting.  Scalar functions have the following properties:

Scalar Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `+` | [Conjugate](primitive-functions-a-z/primitive-functions-a-z/conjugate.md) | [Plus (Add)](scalar-dyadic-arithmetic-functions/add.md) |
| `-` | [Negative](scalar-monadic-functions/negative.md) | [Minus (Subtract)](scalar-dyadic-arithmetic-functions/subtract.md) |
| `×` | [Direction (Signum)](scalar-monadic-functions/direction.md) | [Times (Multiply)](scalar-dyadic-arithmetic-functions/multiply.md) |
| `÷` | [Reciproca](scalar-monadic-functions/reciprocal.md) l | [Divide](scalar-dyadic-arithmetic-functions/divide.md) |
| `|` | [Magnitude](scalar-monadic-functions/magnitude.md) | [Residue](scalar-dyadic-arithmetic-functions/residue.md) |
| `⌊` | [Floor](scalar-monadic-functions/floor.md) | [Minimum](scalar-dyadic-arithmetic-functions/minimum.md) |
| `⌈` | [Ceiling](scalar-monadic-functions/ceiling.md) | [Maximum](scalar-dyadic-arithmetic-functions/maximum.md) |
| `*` | [Exponential](scalar-monadic-functions/exponential.md) | [Power](scalar-dyadic-arithmetic-functions/power.md) |
| `⍟` | [Natural Logarithm](scalar-monadic-functions/natural-logarithm.md) | [Logarithm](scalar-dyadic-arithmetic-functions/logarithm.md) |
| `○` | [Pi Times](scalar-monadic-functions/pi-times.md) | [Circular](circular.md) |
| `!` | [Factorial](scalar-monadic-functions/factorial.md) | [Binomial](scalar-dyadic-arithmetic-functions/binomial.md) |
| `~` | [Not](scalar-monadic-functions/not.md) | $ |
| `?` | [Roll](scalar-monadic-functions/roll.md) | $ |
| `∊` | [Type](scalar-monadic-functions/type.md) (See [Enlist](non-scalar-monadic-structural-functions/enlist.md) ) | $ |
| `^` |  | [And](scalar-dyadic-logical-functions/and-lowest-common-multiple.md) |
| `∨` |  | [Or](scalar-dyadic-logical-functions/or-greatest-common-divisor.md) |
| `⍲` |  | [Nand](scalar-dyadic-logical-functions/nand.md) |
| `⍱` |  | [Nor](scalar-dyadic-logical-functions/nor.md) |
| `<` |  | [Less](scalar-dyadic-logical-functions/less.md) |
| `≤` |  | [Less Or Equal](scalar-dyadic-logical-functions/less-or-equal.md) |
| `=` |  | [Equal](scalar-dyadic-logical-functions/equal.md) |
| `≥` |  | [Greater Or Equal](scalar-dyadic-logical-functions/greater-or-equal.md) |
| `>` |  | [Greater](scalar-dyadic-logical-functions/greater.md) |
| `≠` |  | [Not Equal](scalar-dyadic-logical-functions/not-equal.md) |
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
