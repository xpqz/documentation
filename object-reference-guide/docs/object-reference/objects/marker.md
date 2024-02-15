




<h1 class="heading"><span class="name">Marker</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | A graphical object used to draw polymarkers. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Children | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Properties | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Methods | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Events | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |


Description


The [Points](../a-z/points.md) property specifies one or more sets of points at which one or more sets of polymarkers are to be drawn.



The [Style](../a-z/style.md) property determines the symbol that is drawn at each of a set of points. Marker styles are specified either by numbers which represent the following symbol shapes .

| 0 | . |
| --- | ---  |
| 1 | `+` |
| 2 | `*` |
| 3 | `⎕` |
| 4 | `×` |
| 5 | `⋄` |
| 6 | `∘` |


or by character vectors containing the names of [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) objects.


The height of each symbol is specified by the value of the [Size](../a-z/size.md) property. However this applies only to [Style](../a-z/style.md)s 1-6 and is ignored if [Style](../a-z/style.md) is 0 or the name of a [Bitmap](../a-z/bitmap.md). The colour of each symbol is specified by the [FCol](../a-z/fcol.md) property. The default is black.


The value of [Dragable](../a-z/dragable.md) determines whether or not the object can be dragged. The value of [AutoConf](../a-z/autoconf.md) determines whether or not the Marker object is resized when its parent is resized.


The structure of the property values is best considered separately for single and multiple sets of polymarkers.

#### Single Set of Polymarkers


For a single set of polymarkers, [Points](../a-z/points.md) is either a 2-column matrix of (y,x) co-ordinates, or a 2-element vector of y and x co-ordinates respectively.


[Style](../a-z/style.md) and [Size](../a-z/size.md) are both simple scalar numbers.


[FCol](../a-z/fcol.md) is either a single number representing a standard colour, or a 3-element vector which specifies the marker colour explicitly in terms of RGB values.

#### Examples:


First make a [Form](../a-z/form.md):
```apl
      'F' ⎕WC 'Form'
```


Draw a point at (y=20, x=10):
```apl
      'F.M1' ⎕WC 'Marker' (20 10)
```


Draw a row of points at (y=20, x=10, 20, ... 90) : (Note scalar extension of y-coordinate)
```apl
      'F.M1' ⎕WC 'Marker' (20(10×⍳9))
```


Draw "+" symbols at each corner of a box:
```apl
      Y ← 10 10 50 50
      X ← 10 50 50 10
      'F.M1' ⎕WC 'Marker' (Y X) 1
```


Ditto, but draw them 10% high:
```apl
      'F.M1' ⎕WC 'Marker' (Y X) 1 10
```


Ditto, but use "*" symbols in green:
```apl
      'F.M1' ⎕WC 'Marker' (Y X) 2 10 (0 255 0)
```


#### Multiple Sets of Polymarkers


To draw multiple sets of polymarkers with a single name, [Points](../a-z/points.md) is a nested vector whose items are themselves 2-column matrices or 2-element nested vectors.


[Style](../a-z/style.md) and [Size](../a-z/size.md) may be simple scalars specifying a single type and/or size of symbol to be used for all the sets of polymarkers, or vectors specifying different symbols and/or sizes for each set.


[FCol](../a-z/fcol.md) may be a single number or a single (enclosed) 3-element vector applying to all the sets of polymarkers. Alternatively, [FCol](../a-z/fcol.md) may be a vector whose elements refer to each of the sets of polymarkers in turn. If so, the elements may be single numbers or nested RGB triplets, or a combination of the two.


#### Examples:



First make a [Form](../a-z/form.md):
```apl
      'F' ⎕WC 'Form'
```




Draw a "`⎕`" at (10,20) and a "`⋄`" at (20,20):
```apl
      'F.M1' ⎕WC 'Marker'((1 2⍴10 20)(1 2⍴20 20)) (3 5)
```




Draw "+" symbols at each corner of one box and  "`○`" symbols at each corner of another:
```apl
      Y1 X1 ← (10 10 50 50) (10 50 50 10)
      Y2 X2 ← (20 20 40 40) (20 40 40 20)
      'F.M1' ⎕WC 'Marker' ((Y1 X1)(Y2 X2)) (1 6)
```




Ditto, but draw the "+" symbols with height 2% and the "`○`" symbols 5%:
```apl
      'F.M1' ⎕WC 'Marker' ((Y1 X1)(Y2 X2)) (1 6) (2 5)
```




Ditto, but draw the "+" symbols in red and the "`○`" symbols in blue:
```apl
      'F.M1' ⎕WC 'Marker' ((Y1 X1)(Y2 X2)) (1 6) (2 5)
                          ('FCol' (255 0 0)(0 0 255))
```



