




<h1 class="heading"><span class="name">FStyle</span></h1>

Applies To: [Circle](../a-z/circle.md) [Ellipse](../a-z/ellipse.md) [Poly](../a-z/poly.md) [Rect](../a-z/rect.md)


**Description**


This property determines how a graphics object is filled. It takes one of the following values, or, if the object has more than one component, a vector of such values.


| FStyle | Effect |
| --- | ---  |
| `¯1` | hollow (no fill). This is the default. |
| `0` | solid fill |
| `1` | hatch fill with horizontal lines |
| `2` | hatch fill with vertical lines |
| `3` | hatch fill with diagonal lines at 135 degrees |
| `4` | hatch fill with diagonal lines at 45 degrees |
| `5` | hatch fill with horizontal and vertical lines |
| `6` | hatch fill with criss-crossing diagonal lines |
| `str` | the name of. or a ref to, a [Bitmap](../a-z/bitmap.md) object which is used to fill the object. |


For example, to fill an object with criss-crossing diagonal lines you would specify `('FStyle' 6)`. If the object contained two components, you could fill the first one with criss-crossing diagonal lines, and the second one with a [Bitmap](../a-z/bitmap.md) called `'YES'`, with the specification `('FStyle' 6 'YES')`


If the size of the [Bitmap](../a-z/bitmap.md) is 8x8 APL uses a Windows "brush" to fill the object. If not, it uses "tiling". Filling with a brush is faster.



