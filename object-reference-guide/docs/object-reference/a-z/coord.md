




<h1 class="heading"><span class="name">Coord</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Bitmap](./bitmap.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Circle](./circle.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Font](./font.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Image](./image.md) [ImageList](./imagelist.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Locator](./locator.md) [Marker](./marker.md) [MDIClient](./mdiclient.md) [Menu](./menu.md) [Metafile](./metafile.md) [Poly](./poly.md) [Printer](./printer.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [Text](./text.md) [ToolBar](./toolbar.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Image](./image.md) | [ImageList](./imagelist.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) | [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [Metafile](./metafile.md) | [Poly](./poly.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [Text](./text.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) |
| [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) |
| [Circle](./circle.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Ellipse](./ellipse.md) | [Font](./font.md) | [Form](./form.md) |
| [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) |
| [Image](./image.md) | [ImageList](./imagelist.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) |
| [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) |
| [Metafile](./metafile.md) | [Poly](./poly.md) | [Printer](./printer.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) |
| [Rect](./rect.md) | [RichEdit](./richedit.md) | [Root](./root.md) |
| [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) |
| [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) |
| [Text](./text.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


This property defines an object's co-ordinate system. It is a character
string with one of the following values;`'Inherit'`,
`'Prop'`, `'Pixel'`,
`'RealPixel'`, `'ScaledPixel'`, `'User'` or `'Cell'` (graphics children of a [Grid](./grid.md) only).



If Coord is `'Inherit'`, the co-ordinate
system for the object is inherited from its parent. Note that the default
value of Coord for the system object `'.'` is `'Prop'`, so by default all objects
created by `⎕WC` inherit `'Prop'`.


If Coord is `'Prop'`, the origin of the
object's parent is deemed to be at its top left interior corner, and the scale
along its x- and y-axes is 100. The object's position and size ([Posn](./posn.md) and [Size](./size.md) properties) are therefore specified
and reported as a percentage of the dimensions of the parent object, or, for a [Form](./form.md),
of the screen.


If Coord is `'RealPixel'`, the origin of the
object's parent is deemed to be at its top left interior corner, and the scale
along its x- and y-axes is measured in physical pixel units. The object's position
and size (Posn and Size properties) are therefore reported and set in physical pixel units. If you set
Coord on the system object to `'Pixel'`, the
value of its Size property gives you the
resolution of your screen. Note that pixels are numbered from 0
to (Size -1).


If Coord is `'ScaledPixel'`  the number of pixels specified for Posn, Size,  and other such properties will be automatically scaled by Dyalog APL according to the user's chosen display scaling factor. So if you specify an Edit object to be 80 pixels wide and 20 pixels high, and the user's scaling factor is 150%, Dyalog will automatically draw it 120 pixels wide and 30 pixels high. Dyalog will also de-scale coordinate values reported by `⎕WG` and  event messages.


If Coord is `'User'`, the origin and
scale of the co-ordinate system are defined by the values of the YRange and XRange properties of the parent
object. Each of these is a 2-element numeric vector whose elements define
the co-ordinates of top left and bottom right interior corners of the (parent)
object respectively.


Note that if Coord is `'User'` and you
change the values of YRange and/or XRange of the parent, the object (and all its siblings with Coord `'User'`)
are redrawn (and clipped) according to the new origin and scale defined for the
parent. The values of their Posn, Size and Points properties are unaffected.
Changing YRange and/or XRange therefore provides a convenient and efficient means to "pan and zoom".


The Coord property for graphic objects created as  children of a Grid may
also be set to Cell. Apart from being easier to compute, a graphic drawn using
cell coordinates will expand and contract when the grid rows and columns are
resized.


#### Example:


This statement creates a button 10 pixels high, 20 pixels wide, and 5 pixels
down and along from the top-left corner of the parent [Form](./form.md) T.
```apl
      'T.B1'⎕WC'Button' 'OK'(5 5)(10 20)('Coord' 'Pixel')
```




If you set Coord to `'RealPixel'` in the [Root](./root.md) object `'.'`, then query its Size,
you get the dimensions of the screen in pixels, i.e.
```apl
      '.' ⎕WS 'Coord' 'RealPixel'
      '.' ⎕WG 'Size'
480 640
```




If you set Coord to `'ScaledPixel'` in the [Root](./root.md) object `'.'`, then query its Size,
you get the virtual resolution of the screen, i.e.
```apl
      '.'⎕WS 'Coord' 'ScaledPixel'
      '.'⎕WG'Size'
1080 1920

```



If Coord is `'Pixel'`, it is interpreted as either `'RealPixel'` or `'ScaledPixel'` according to the value of the Dyalog_Pixel_Type parameter, which is either ScaledPixel or RealPixel. See 
Installation & Configuration Guide: 

Dyalog_Pixel_Type parameterDyalog_Pixel_Type on page 1.


If this parameter is not specified, the default is RealPixel. So by default, when you set Coord to Pixel, it will be treated as RealPixel.


