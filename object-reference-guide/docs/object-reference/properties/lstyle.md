




<h1 class="heading"><span class="name">LStyle</span></h1>

| Applies To: | [Circle](../a-z/circle.md) | [Ellipse](../a-z/ellipse.md) | [Locator](../a-z/locator.md) | [Poly](../a-z/poly.md) | [Rect](../a-z/rect.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


This property determines the type of line used to draw a graphics object. It takes one of the following integer values, or, if the object contains more than one component, a vector of such values.


| 0 | solid line |
| --- | ---  |
| 1 | dashed line |
| 2 | dotted line |
| 3 | dash dotted line |
| 4 | dash dot dotted line |
| 5 | null line (invisible) |


If LStyle is in the range 1-4, the gaps between the dashes and dots are drawn using the colour specified by [BCol](../a-z/bcol.md), or are left undrawn (i.e. transparent) if [BCol](../a-z/bcol.md) is not defined.


In versions of Dyalog APL prior to 13.2 revision 19489, if LWidth specified a line width greater than 1 pixel, a solid line was drawn in the colour specified by the FCol Property, regardless of the value of [LStyle](../a-z/lstyle.md). From that revision onwards, if the value of LWidth is greater than 1  then the value of LStyle is honoured, but only the FCol of the line is honoured - the BCol is still ignored.



