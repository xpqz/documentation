




<h1 class="heading"><span class="name">Coord</span></h1>

**Applies To**


**Description**


This property defines an object's co-ordinate system. It is a character
string with one of the following values;`'Inherit'`,
`'Prop'`, `'Pixel'`,
`'RealPixel'`, `'ScaledPixel'`, `'User'` or `'Cell'` (graphics children of a [Grid](../a-z/grid.md) only).



If Coord is `'Inherit'`, the co-ordinate
system for the object is **inherited** from its parent. Note that the default
value of Coord for the system object `'.'` is `'Prop'`, so by default all objects
created by [`⎕WC`](../../Language/System Functions/wc.htm) inherit `'Prop'`.


If Coord is `'Prop'`, the origin of the
object's parent is deemed to be at its top left interior corner, and the scale
along its x- and y-axes is 100. The object's position and size ([Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties) are therefore specified
and reported as a percentage of the dimensions of the parent object, or, for a [Form](../a-z/form.md),
of the screen.


If Coord is `'RealPixel'`, the origin of the
object's parent is deemed to be at its top left interior corner, and the scale
along its x- and y-axes is measured in physical pixel units. The object's position
and size ([Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties) are therefore reported and set in physical pixel units. If you set
Coord on the system object to `'Pixel'`, the
value of its [Size](../a-z/size.md) property gives you the
resolution of your screen. Note that pixels are numbered from 0
to (Size -1).


If Coord is `'ScaledPixel'`  the number of pixels specified for [Posn](../a-z/posn.md), [Size](../a-z/size.md),  and other such properties will be automatically scaled by Dyalog APL according to the user's chosen display scaling factor. So if you specify an Edit object to be 80 pixels wide and 20 pixels high, and the user's scaling factor is 150%, Dyalog will automatically draw it 120 pixels wide and 30 pixels high. Dyalog will also de-scale coordinate values reported by `⎕WG` and  event messages.


If Coord is `'User'`, the origin and
scale of the co-ordinate system are defined by the values of the [YRange](../a-z/yrange.md) and [XRange](../a-z/xrange.md) properties **of the parent
object**. Each of these is a 2-element numeric vector whose elements define
the co-ordinates of top left and bottom right interior corners of the (parent)
object respectively.


Note that if Coord is `'User'` and you
change the values of [YRange](../a-z/yrange.md) and/or [XRange](../a-z/xrange.md) of the parent, the object (and all its siblings with Coord `'User'`)
are redrawn (and clipped) according to the new origin and scale defined for the
parent. The values of their [Posn](../a-z/posn.md), [Size](../a-z/size.md) and [Points](../a-z/points.md) properties are unaffected.
Changing [YRange](../a-z/range.md) and/or [XRange](../a-z/range.md) therefore provides a convenient and efficient means to "**pan and zoom**".


The Coord property for graphic objects created as  children of a Grid may
also be set to Cell. Apart from being easier to compute, a graphic drawn using
cell coordinates will expand and contract when the grid rows and columns are
resized.


#### Example:


This statement creates a button 10 pixels high, 20 pixels wide, and 5 pixels
down and along from the top-left corner of the parent [Form](../a-z/form.md) T.
```apl
      'T.B1'⎕WC'Button' 'OK'(5 5)(10 20)('Coord' 'Pixel')
```




If you set Coord to `'RealPixel'` in the [Root](../a-z/root.md) object `'.'`, then query its [Size](../a-z/size.md),
you get the dimensions of the screen in pixels, i.e.
```apl
      '.' ⎕WS 'Coord' 'RealPixel'
      '.' ⎕WG 'Size'
480 640
```




If you set Coord to `'ScaledPixel'` in the [Root](../a-z/root.md) object `'.'`, then query its [Size](../a-z/size.md),
you get the virtual resolution of the screen, i.e.
```apl
      '.'⎕WS 'Coord' 'ScaledPixel'
      '.'⎕WG'Size'
1080 1920

```



If Coord is `'Pixel'`, it is interpreted as either `'RealPixel'` or `'ScaledPixel'` according to the value of the Dyalog_Pixel_Type parameter, which is either ScaledPixel or RealPixel. See 
Installation & Configuration Guide: 

Dyalog_Pixel_Type parameter[Dyalog_Pixel_Type](../../../UserGuide/Installation and Configuration/Configuration Parameters/Dyalog_Pixel_Type.htm#Dyalog_Pixel_Type).


**If this parameter is not specified, the default is RealPixel. So by default, when you set Coord to Pixel, it will be treated as RealPixel.**


