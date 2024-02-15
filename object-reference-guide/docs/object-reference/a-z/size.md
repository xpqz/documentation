



<h1 class="heading"><span class="name">Size</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Bitmap](./bitmap.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBand](./coolband.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Font](./font.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Icon](./icon.md) [Image](./image.md) [ImageList](./imagelist.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Locator](./locator.md) [Marker](./marker.md) [MDIClient](./mdiclient.md) [Metafile](./metafile.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabButton](./tabbutton.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Icon](./icon.md) | [Image](./image.md) | [ImageList](./imagelist.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) | [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Metafile](./metafile.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) |
| [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) |
| [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Font](./font.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [HTMLRenderer](./htmlrenderer.md) | [Icon](./icon.md) | [Image](./image.md) |
| [ImageList](./imagelist.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Locator](./locator.md) | [Marker](./marker.md) |
| [MDIClient](./mdiclient.md) | [Metafile](./metafile.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [Rect](./rect.md) |
| [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) |
| [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


This is a 2-element numeric vector specifying the height and width of the object.


For the [Bitmap](./bitmap.md) object, Size is set and reported in pixels. Setting the Size of a [Bitmap](./bitmap.md) causes it to be scaled (up or down).


For all other objects, Size is reported and set in units defined by the [Coord](coord.md) property and, if [Coord](coord.md) is `'User'`, the XRange and YRange properties of the object's parent.


For the [Root](./root.md) object, if [Coord](coord.md) is `'Prop'` the value of Size is (100,100). If [Coord](coord.md) is `'Pixel'` the value of Size reports the number of pixels on the screen.


For a [Form](./form.md) or [SubForm](./subform.md), the Size property defines the area within the object, and excludes its title bar, menu bar and border if these are present.


For a [Combo](./combo.md) object with a "drop-down" list, the first element of Size (height) is ignored. The height of the edit field is determined by the height of the font, while the size of the list box is determined by the Rows property.


Otherwise the Size property defines the total size of the object, including borders, edges etc.


When specifying Size, you can set the height or width to a default value (`⎕WC`) or leave it unchanged (`⎕WS`) by giving the corresponding element a value of `⍬`.


