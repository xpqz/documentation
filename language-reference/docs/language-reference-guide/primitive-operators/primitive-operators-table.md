# Primitive Operators

| Glyph | Glyph Name | Operator | Syntax |
| --- | --- | --- | ---  |
| `[]←` |  | Assignment Indexed Modified | `{R}←X[I]f←Y` |
| `←` | Left Arrow | Assignment Modified | `{R}←Xf←Y` |
| `←` | Left Arrow | Assignment Selective Modified | `{R}←(EXP X)f←Y` |
| `@` | At | [At](../system-functions/system-functions-a-z/system-functions-a-z/at.md) | `R←{X}(f@g)Y` |
| `⍤` | Jot Diaeresis | Atop | `{R}←{X}f⍤gY` |
| `[]` |  | Axis with Dyadic Operand | `R←Xf[B]Y` |
| `[]` |  | Axis with Monadic Operand | `R←f[B]Y` |
| `∘` | Jot | Beside | `{R}←{X}f∘gY` |
| `∘` | Jot | Bind | `{R}←A∘fY {R}←(f∘B)Y` |
| `⍨` | Tilde Diaeresis | Commute | `{R}←{X}f⍨Y` |
| `⍨` | Tilde Diaeresis | Constant | `R←{X}(A⍨)Y` |
| `¨` | Diaeresis | Each with Dyadic Operand | `{R}←Xf¨Y` |
| `¨` | Diaeresis | Each with Monadic Operand | `{R}←f¨Y` |
| `⌶` | IBeam | [I-Beam](../the-i-beam-operator/i-beam.md) | `R←{X}(A⌶)Y` |
| `.` | Dot | Inner Product | `R←Xf.gY` |
| `⌸` | Quad Equal | Key | `R←{X}f⌸Y` |
| `∘.` |  | Outer Product | `{R}←X∘.gY` |
| `⍥` | Circle Dieresis | Over | `{R}←{X}f⍥gY` |
| `⍣` | Star Diaeresis | Power Operator | `{R}←{X}(f⍣g)Y` |
| `⍤` | Jot Diaeresis | Rank | `R←{X}(f⍤B)Y` |
| `⌿` | Slash Bar | Reduce First N Wise | `R←Xf⌿[K]Y` |
| `⌿` | Slash Bar | Reduce First | `R←f⌿Y` |
| `/` | Slash | Reduce N Wise | `R←Xf/[K]Y` |
| `/` | Slash | Reduce | `R←f/[K]Y` |
| `⍀` | Slope Bar | Scan First | `R←f⍀Y` |
| `\` | Slope | Scan | `R←f\[K]Y` |
| `&` | Ampersand | Spawn | `{R}←{X}f&Y` |
| `⌺` | Quad Diamond | Stencil | `R←(f⌺g)Y` |
| `⍠` | Variant | Variant | `{R}←{X}(f⍠B)Y` |
