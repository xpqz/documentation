




<h1 class="heading"><span class="name">End</span></h1>

| Applies To: | [Circle](./circle.md) | [Ellipse](./ellipse.md) |
| --- | --- | ---  |


**Description**


This property specifies one or more end-angles for an arc, pie-slice, or chord of a circle or ellipse. It may be used in conjunction with [Start](Start.htm) which specifies start angles. Angles are measured counter-clockwise from the x-axis at the centre of the object.


If a single arc is being drawn, End is a single number that specifies the end angle of the arc in radians `(0 ⍎> ○2)`. If multiple arcs are being drawn, End is either a single number as before (the end angle for several concentric arcs) or a numeric vector with one element per arc.


If [Start](Start.htm) is not specified, the default value of End is `○2`. Otherwise, the default value of End is `((¯1↓+\Start),○2)`.



