# Mixed Functions

Mixed rank functions and special symbols are summarised in [Table 1](#MixedRankFunctions). For convenience, they are sub-divided into five classes:

Mixed rank functions and special symbols

| **Structural** | These functions change the structure of the arguments in some way. |
| --- | ---  |
| **Selection** | These functions select elements from an argument. |
| **Selector** | These functions identify specific elements by a Boolean map or by an ordered set of indices. |
| **Miscellaneous** | These functions transform arguments in some way, or provide information about the arguments. |
| **Special** | These symbols have special properties. |

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
| `⍴` | $ | [Reshape](Reshape.htm) |
| `,` | [Ravel ](Ravel.htm) `[]` | [Catenate/Laminate](Catenate Laminate.htm) `[]` |
| `⍪` | [Table](Table.htm) | [Catenate First / Laminate ](Catenate First.htm) `[]` |
| `⌽` | [Reverse ](Reverse.htm) `[]` | [Rotate ](Rotate.htm) `[]` |
| `⊖` | [Reverse First ](Reverse First.htm) `[]` | [Rotate First ](Rotate First.htm) `[]` |
| `⍉` | [Transpose](Transpose Monadic.htm) | [Transpose](Transpose Dyadic.htm) |
| `↑` | [Mix](Mix.htm) / [Disclose ](Disclose.htm) `[]` | $ |
| `↓` | [Split ](Split.htm) `[]` | $ |
| `⊂` | [Enclose ](Enclose.htm) `[]` | [Partitioned Enclose ](Partitioned Enclose.htm) `[]` |
| `⊆` | [Nest](Nest.htm) | [Partition ](Partition.htm) `[]` |
| `∊` | [Enlist](Enlist.htm) (See [Type](Type.htm) ) | $ |

Selection Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⊃` | [Disclose ](Disclose.htm) / [Mix](Mix.htm) | [Pick](Pick.htm) |
| `↑` | $ | [Take ](Take.htm) `[]` |
| `↓` | $ | [Drop ](../system-commands/system-commands-a-z/drop.md) `[]` |
| `/` |  | [Replicate ](Replicate.htm) `[]` |
| `⌿` |  | [Replicate First ](Replicate First.htm) `[]` |
| `\` |  | [Expand ](Expand.htm) `[]` |
| `⍀` |  | [Expand First ](Expand First.htm) `[]` |
| `~` | $ | [Without (Excluding)](Excluding.htm) |
| `∩` |  | [Intersection](Intersection.htm) |
| `∪` | [Unique](Unique.htm) | [Union](Union.htm) |
| `⊣` | [Same](Same.htm) | [Left](Left.htm) |
| `⊢` | [Same](Same.htm) | [Right](Right.htm) |
| `⌷` | [Materialise](Materialise.htm) | [Index](../../index.md) |
| `≠` | [Unique Mask](Unique Mask.htm) |  |

Selector Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍳` | [Index Generator](Index Generator.htm) | [Index Of](Index Of.htm) |
| `⍸` | [Where](Where.htm) | [Interval Index](Interval Index.htm) |
| `∊` | $ | [Membership](Membership.htm) |
| `⍋` | [Grade Up](Grade Up Monadic.htm) | [Grade Up](Grade Up Dyadic.htm) |
| `⍒` | [Grade Down](Grade Down Monadic.htm) | [Grade Down](Grade Down Dyadic.htm) |
| `?` | $ | [Deal](Deal.htm) |
| `⍷` |  | [Find](Find.htm) |

Miscellaneous Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍴` | [Shape](Shape.htm) | $ |
| `≡` | [Depth](Depth.htm) | [Match](Match.htm) |
| `≢` | [Tally](Tally.htm) | [Not Match](Not Match.htm) |
| `⍎` | [Execute](Execute.htm) | [Execute](Execute.htm) |
| `⍕` | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-monadic.md) | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-dyadic.md) |
| `⊥` |  | [Decode (Base)](Decode.htm) |
| `⊤` |  | [Encode (Representation)](Encode.htm) |
| `⌹` | [Matrix Inverse](Matrix Inverse.htm) | [Matrix Divide](Matrix Divide.htm) |

Special Syntax

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `→` | [Abort](Abort.htm) |  |
| `→` | [Branch](Branch.htm) |  |
| `←` |  | [Assignment](Assignment.htm) |
| `[I]←` |  | [Assignment(Indexed)](Assignment Indexed.htm) |
| `(I)←` |  | [Assignment(Selective)](Assignment Selective.htm) |
| `[]` |  | [Indexing](Indexing.htm) |
