# Mixed Functions

Mixed rank functions and special symbols are summarised in Table 1. For convenience, they are sub-divided into five classes:

Mixed rank functions and special symbols

| Structural | These functions change the structure of the arguments in some way. |
| --- | ---  |
| Selection | These functions select elements from an argument. |
| Selector | These functions identify specific elements by a Boolean map or by an ordered set of indices. |
| Miscellaneous | These functions transform arguments in some way, or provide information about the arguments. |
| Special | These symbols have special properties. |

In general, the structure of the result of a mixed primitive function is different from that of its arguments.

Scalar extension may apply to some, but not all, dyadic mixed functions.

Mixed primitive functions are not pervasive. The function is applied to elements of the arguments, not necessarily independently.

### Examples
```apl
      'CAT' 'DOG' 'MOUSE'⍳⊂'DOG'
2 
      3↑ 1 'TWO' 3 'FOUR'
1  TWO  3
```

In the following tables, note that:

- `[]` Implies axis specification is optional
- $  This function is in another class

Structural Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍴` | $ | Reshape |
| `,` | Ravel `[]` | Catenate/Laminate `[]` |
| `⍪` | Table | Catenate First / Laminate `[]` |
| `⌽` | Reverse `[]` | Rotate `[]` |
| `⊖` | Reverse First `[]` | Rotate First `[]` |
| `⍉` | Transpose | Transpose |
| `↑` | Mix / Disclose `[]` | $ |
| `↓` | Split `[]` | $ |
| `⊂` | Enclose `[]` | Partitioned Enclose `[]` |
| `⊆` | Nest | Partition `[]` |
| `∊` | Enlist (See Type ) | $ |

Selection Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⊃` | Disclose / Mix | Pick |
| `↑` | $ | Take `[]` |
| `↓` | $ | [Drop ](../system-commands/system-commands-a-z/drop.md) `[]` |
| `/` |  | Replicate `[]` |
| `⌿` |  | Replicate First `[]` |
| `\` |  | Expand `[]` |
| `⍀` |  | Expand First `[]` |
| `~` | $ | Without (Excluding) |
| `∩` |  | Intersection |
| `∪` | Unique | Union |
| `⊣` | Same | Left |
| `⊢` | Same | Right |
| `⌷` | Materialise | [Index](../../index.md) |
| `≠` | Unique Mask |  |

Selector Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍳` | Index Generator | Index Of |
| `⍸` | Where | Interval Index |
| `∊` | $ | Membership |
| `⍋` | Grade Up | Grade Up |
| `⍒` | Grade Down | Grade Down |
| `?` | $ | Deal |
| `⍷` |  | Find |

Miscellaneous Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍴` | Shape | $ |
| `≡` | Depth | Match |
| `≢` | Tally | Not Match |
| `⍎` | Execute | Execute |
| `⍕` | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-monadic.md) | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-dyadic.md) |
| `⊥` |  | Decode (Base) |
| `⊤` |  | Encode (Representation) |
| `⌹` | Matrix Inverse | Matrix Divide |

Special Syntax

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `→` | Abort |  |
| `→` | Branch |  |
| `←` |  | Assignment |
| `[I]←` |  | Assignment(Indexed) |
| `(I)←` |  | Assignment(Selective) |
| `[]` |  | Indexing |
