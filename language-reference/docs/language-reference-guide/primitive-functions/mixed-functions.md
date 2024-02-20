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
| `⍴` | $ | [Reshape](non-scalar-dyadic-structural-functions/reshape.md) |
| `,` | [Ravel ](non-scalar-monadic-structural-functions/ravel.md) `[]` | [Catenate/Laminate](non-scalar-dyadic-structural-functions/catenate-laminate.md) `[]` |
| `⍪` | [Table](non-scalar-monadic-structural-functions/table.md) | [Catenate First / Laminate ](primitive-functions-a-z/primitive-functions-a-z/catenate-first.md) `[]` |
| `⌽` | [Reverse ](non-scalar-monadic-structural-functions/reverse.md) `[]` | [Rotate ](non-scalar-dyadic-structural-functions/rotate.md) `[]` |
| `⊖` | [Reverse First ](primitive-functions-a-z/primitive-functions-a-z/reverse-first.md) `[]` | [Rotate First ](primitive-functions-a-z/primitive-functions-a-z/rotate-first.md) `[]` |
| `⍉` | [Transpose](non-scalar-monadic-structural-functions/transpose-monadic.md) | [Transpose](non-scalar-dyadic-structural-functions/transpose-dyadic.md) |
| `↑` | [Mix](non-scalar-monadic-structural-functions/mix.md) / [Disclose ](non-scalar-selection-functions/disclose.md) `[]` | $ |
| `↓` | [Split ](non-scalar-monadic-structural-functions/split.md) `[]` | $ |
| `⊂` | [Enclose ](non-scalar-monadic-structural-functions/enclose.md) `[]` | [Partitioned Enclose ](non-scalar-dyadic-structural-functions/partitioned-enclose.md) `[]` |
| `⊆` | [Nest](non-scalar-monadic-structural-functions/nest.md) | [Partition ](non-scalar-dyadic-structural-functions/partition.md) `[]` |
| `∊` | [Enlist](non-scalar-monadic-structural-functions/enlist.md) (See [Type](scalar-monadic-functions/type.md) ) | $ |

Selection Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⊃` | [Disclose ](non-scalar-selection-functions/disclose.md) / [Mix](non-scalar-monadic-structural-functions/mix.md) | [Pick](non-scalar-selection-functions/pick.md) |
| `↑` | $ | [Take ](non-scalar-selection-functions/take.md) `[]` |
| `↓` | $ | [Drop ](../system-commands/system-commands-a-z/drop.md) `[]` |
| `/` |  | [Replicate ](non-scalar-selection-functions/replicate.md) `[]` |
| `⌿` |  | [Replicate First ](Replicate First.htm) `[]` |
| `\` |  | [Expand ](non-scalar-selection-functions/expand.md) `[]` |
| `⍀` |  | [Expand First ](primitive-functions-a-z/primitive-functions-a-z/expand-first.md) `[]` |
| `~` | $ | [Without (Excluding)](non-scalar-selection-functions/excluding.md) |
| `∩` |  | [Intersection](non-scalar-selection-functions/intersection.md) |
| `∪` | [Unique](non-scalar-selection-functions/unique.md) | [Union](non-scalar-selection-functions/union.md) |
| `⊣` | [Same](non-scalar-selection-functions/same.md) | [Left](non-scalar-selection-functions/left.md) |
| `⊢` | [Same](non-scalar-selection-functions/same.md) | [Right](non-scalar-selection-functions/right.md) |
| `⌷` | [Materialise](Materialise.htm) | [Index](../../index.md) |
| `≠` | [Unique Mask](non-scalar-selection-functions/unique-mask.md) |  |

Selector Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍳` | [Index Generator](non-scalar-selector-functions/index-generator.md) | [Index Of](non-scalar-selector-functions/index-of.md) |
| `⍸` | [Where](non-scalar-selector-functions/where.md) | [Interval Index](non-scalar-selector-functions/interval-index.md) |
| `∊` | $ | [Membership](non-scalar-selector-functions/membership.md) |
| `⍋` | [Grade Up](non-scalar-selector-functions/grade-up-monadic.md) | [Grade Up](non-scalar-selector-functions/grade-up-dyadic.md) |
| `⍒` | [Grade Down](non-scalar-selector-functions/grade-down-monadic.md) | [Grade Down](non-scalar-selector-functions/grade-down-dyadic.md) |
| `?` | $ | [Deal](non-scalar-selector-functions/deal.md) |
| `⍷` |  | [Find](non-scalar-selector-functions/find.md) |

Miscellaneous Primitive Functions

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `⍴` | [Shape](non-scalar-monadic-structural-functions/shape.md) | $ |
| `≡` | [Depth](non-scalar-monadic-structural-functions/depth.md) | [Match](non-scalar-selector-functions/match.md) |
| `≢` | [Tally](non-scalar-monadic-structural-functions/tally.md) | [Not Match](non-scalar-selector-functions/not-match.md) |
| `⍎` | [Execute](non-scalar-computational-functions/execute.md) | [Execute](non-scalar-computational-functions/execute.md) |
| `⍕` | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-monadic.md) | [Format](../system-functions/system-functions-a-z/system-functions-a-z/format-dyadic.md) |
| `⊥` |  | [Decode (Base)](non-scalar-computational-functions/decode.md) |
| `⊤` |  | [Encode (Representation)](non-scalar-computational-functions/encode.md) |
| `⌹` | [Matrix Inverse](non-scalar-computational-functions/matrix-inverse.md) | [Matrix Divide](non-scalar-computational-functions/matrix-divide.md) |

Special Syntax

| Symbol | Monadic | Dyadic |
| --- | --- | ---  |
| `→` | [Abort](non-scalar-computational-functions/abort.md) |  |
| `→` | [Branch](non-scalar-computational-functions/branch.md) |  |
| `←` |  | [Assignment](primitive-functions-a-z/primitive-functions-a-z/assignment.md) |
| `[I]←` |  | [Assignment(Indexed)](primitive-functions-a-z/primitive-functions-a-z/assignment-indexed.md) |
| `(I)←` |  | [Assignment(Selective)](primitive-functions-a-z/primitive-functions-a-z/assignment-selective.md) |
| `[]` |  | [Indexing](primitive-functions-a-z/primitive-functions-a-z/indexing.md) |
