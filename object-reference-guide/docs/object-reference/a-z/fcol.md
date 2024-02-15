




<h1 class="heading"><span class="name">FCol</span></h1>

Applies To

| Applies To: | [ActiveXContainer](./activexcontainer.md) [ActiveXControl](./activexcontrol.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Circle](./circle.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBand](./coolband.md) [CoolBar](./coolbar.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Marker](./marker.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [Poly](./poly.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Separator](./separator.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [TabBtn](./tabbtn.md) [Text](./text.md) [TipField](./tipfield.md) [ToolBar](./toolbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXContainer](./activexcontainer.md) | [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Circle](./circle.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Marker](./marker.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [Poly](./poly.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Separator](./separator.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [TabBtn](./tabbtn.md) | [Text](./text.md) | [TipField](./tipfield.md) | [ToolBar](./toolbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |
| --- | --- | ---  |
| [ActiveXContainer](./activexcontainer.md) | [ActiveXControl](./activexcontrol.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Circle](./circle.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) |
| [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Marker](./marker.md) | [Menu](./menu.md) |
| [MenuItem](./menuitem.md) | [Poly](./poly.md) | [Rect](./rect.md) |
| [RichEdit](./richedit.md) | [Separator](./separator.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [TabBtn](./tabbtn.md) | [Text](./text.md) | [TipField](./tipfield.md) |
| [ToolBar](./toolbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |


Description


This property defines the foreground colour(s) of an object.



For
non-graphical objects, FCol specifies a single colour. For graphical objects
with more than one constituent part, it may specify a set of background colours,
one for each part. A single colour is represented by a single number which
refers to a standard colour, or by a 3-element vector which defines a colour
explicitly in terms of its red, green and blue intensities.


If FCol is 0 (which is the default) the foreground colour is defined by your
current colour scheme for the object in question. For example, if you select red
as your MS-Windows "Button Text" colour, you will by default get red
writing on all your [Button](./button.md) objects, simply by
not specifying FCol or by setting it to 0.


A negative value of FCol refers to a standard MS-Windows colour as described
below. Positive values are reserved for a possible future extension.

| FCol | Colour Element | FCol | Colour Element |
| --- | --- | --- | ---  |
| `0` | Default | `¯11` | Active Border |
| `¯1` | Scroll Bars | `¯12` | Inactive Border |
| `¯2` | Desktop | `¯13` | Application Workspace |
| `¯3` | Active Title Bar | `¯14` | Highlight |
| `¯4` | Inactive Title Bar | `¯15` | Highlighted Text |
| `¯5` | Menu Bar | `¯16` | Button Face |
| `¯6` | Window Background | `¯17` | Button Shadow |
| `¯7` | Window Frame | `¯18` | Disabled Text |
| `¯8` | Menu Text | `¯19` | Button Text |
| `¯9` | Window Text | `¯20` | Inactive Title Bar Text |
| `¯10` | Active Title Bar Text | `¯21` | Button Highlight |


If instead, FCol contains a 3-element vector, it specifies the intensity of
the red, green and blue components of the colour as values in the range 0-255.
For example, (255 0 0) is red and (255 255 0) is yellow.


Note that if the colour specified by FCol would normally be rendered as a
dithered colour, it is instead converted to the nearest pure colour available on
the device. The actual colour realised also depends upon the capabilities of the
display adapter and driver, and the current Windows colour map.


For a [Button](./button.md), [Combo](./combo.md),
[Edit](./edit.md), [Label](./label.md), [List](./list.md),
[Menu](./menu.md) and [MenuItem](./menuitem.md),
FCol refers to the colour of the text in the object. [Border](border.md)s
around these objects (where applicable) are drawn using the standard Windows
colour. For a [Static](./static.md) object however, FCol
specifies the colour of its border.


For the [Ellipse](./ellipse.md), [Poly](./poly.md) and [Rect](./rect.md) objects, FCol specifies the colour of
the line drawn around the perimeter of the object. If a dashed or dotted line is
used ([LStyle](lstyle.md) 1-4) the "gaps" in
the line are drawn using the colour specified by [BCol](bcol.md),
or are left undrawn if [BCol](bcol.md) is not specified.
For the [Marker](./marker.md) object, FCol specifies the
colour in which the markers are drawn. For the graphics objects [Ellipse](./ellipse.md),
[Poly](./poly.md), [Rect](./rect.md) and [Text](./text.md),
FCol may be a vector of 3-element vectors specifying a set of colours for the
constituent parts of the object. For example, a [Poly](./poly.md) object consisting of four polygons, may have a FCol property of four 3-element
vectors. In addition, for graphics objects, FCol is used in place of [FillCol](fillcol.md) if the latter is not specified.


