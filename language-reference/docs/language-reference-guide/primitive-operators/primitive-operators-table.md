# Primitive Operators

| Glyph | Glyph Name | Operator | Syntax |
| --- | --- | --- | ---  |
| `[]←` |  | [Assignment Indexed Modified](operators-a-z/assignment-indexed-modified.md) | `{R}←X[I]f←Y` |
| `←` | Left Arrow | [Assignment Modified](operators-a-z/assignment-modified.md) | `{R}←Xf←Y` |
| `←` | Left Arrow | [Assignment Selective Modified](operators-a-z/assignment-selective-modified.md) | `{R}←(EXP X)f←Y` |
| `@` | At | [At](../system-functions/system-functions-a-z/system-functions-a-z/at.md) | `R←{X}(f@g)Y` |
| `⍤` | Jot Diaeresis | [Atop](operators-a-z/atop.md) | `{R}←{X}f⍤gY` |
| `[]` |  | [Axis with Dyadic Operand](operators-a-z/axis-with-dyadic-operand.md) | `R←Xf[B]Y` |
| `[]` |  | [Axis with Monadic Operand](operators-a-z/axis-with-monadic-operand.md) | `R←f[B]Y` |
| `∘` | Jot | [Beside](operators-a-z/beside.md) | `{R}←{X}f∘gY` |
| `∘` | Jot | [Bind](operators-a-z/bind.md) | `{R}←A∘fY {R}←(f∘B)Y` |
| `⍨` | Tilde Diaeresis | [Commute](operators-a-z/commute.md) | `{R}←{X}f⍨Y` |
| `⍨` | Tilde Diaeresis | [Constant](operators-a-z/constant.md) | `R←{X}(A⍨)Y` |
| `¨` | Diaeresis | [Each with Dyadic Operand](operators-a-z/each-with-dyadic-operand.md) | `{R}←Xf¨Y` |
| `¨` | Diaeresis | [Each with Monadic Operand](operators-a-z/each-with-monadic-operand.md) | `{R}←f¨Y` |
| `⌶` | IBeam | [I-Beam](../the-i-beam-operator/i-beam.md) | `R←{X}(A⌶)Y` |
| `.` | Dot | [Inner Product](operators-a-z/inner-product.md) | `R←Xf.gY` |
| `⌸` | Quad Equal | [Key](operators-a-z/key.md) | `R←{X}f⌸Y` |
| `∘.` |  | [Outer Product](operators-a-z/outer-product.md) | `{R}←X∘.gY` |
| `⍥` | Circle Dieresis | [Over](operators-a-z/over.md) | `{R}←{X}f⍥gY` |
| `⍣` | Star Diaeresis | [Power Operator](operators-a-z/power-operator.md) | `{R}←{X}(f⍣g)Y` |
| `⍤` | Jot Diaeresis | [Rank](operators-a-z/rank.md) | `R←{X}(f⍤B)Y` |
| `⌿` | Slash Bar | [Reduce First N Wise](operators-a-z/reduce-first-n-wise.md) | `R←Xf⌿[K]Y` |
| `⌿` | Slash Bar | [Reduce First](operators-a-z/reduce-first.md) | `R←f⌿Y` |
| `/` | Slash | [Reduce N Wise](operators-a-z/reduce-n-wise.md) | `R←Xf/[K]Y` |
| `/` | Slash | [Reduce](operators-a-z/reduce.md) | `R←f/[K]Y` |
| `⍀` | Slope Bar | [Scan First](operators-a-z/scan-first.md) | `R←f⍀Y` |
| `\` | Slope | [Scan](operators-a-z/scan.md) | `R←f\[K]Y` |
| `&` | Ampersand | [Spawn](operators-a-z/spawn.md) | `{R}←{X}f&Y` |
| `⌺` | Quad Diamond | [Stencil](operators-a-z/stencil.md) | `R←(f⌺g)Y` |
| `⍠` | Variant | [Variant](operators-a-z/variant.md) | `{R}←{X}(f⍠B)Y` |
