




<h1 class="heading"><span class="name">Radius</span></h1>
| Applies To: | [Circle](./circle.md) | [Rect](./rect.md) |
| --- | --- | ---  |

| Applies To: | [Circle](./circle.md) [Rect](./rect.md) | [Circle](./circle.md) | [Rect](./rect.md) |  |
| --- | --- | ---  |
| [Circle](./circle.md) | [Rect](./rect.md) |  |


Description


For a [Circle](./circle.md) object, this property is a single number that specifies the radius of the circle/arc or a numeric vector that specifies the radii of a set of circles/arcs.


For a [Rect](./rect.md) object, Radius is a 2-element vector that specifies the curvature of the corners of the rectangle or set of rectangles to be drawn. The curvature is defined in terms of the vertical and horizontal radii of an ellipse. The first element of Radius defines the radius vertically, the second horizontally. If more than one rectangle is involved, either or both of the elements of Radius may be vectors. The default value is (0,0) which gives square corners.



