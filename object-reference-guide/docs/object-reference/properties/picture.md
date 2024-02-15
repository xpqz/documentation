




<h1 class="heading"><span class="name">Picture</span></h1>

**Applies To**


**Description**


The Picture property specifies a bitmap, icon, or other image for an object.



For [Button](../a-z/button.md), [Form](../a-z/form.md), [Group](../a-z/group.md), [MDIClient](../a-z/mdiclient.md), [Static](../a-z/static.md), [StatusBar](../a-z/statusbar.md), [StatusField](../a-z/statusfield.md), [SubForm](../a-z/subform.md), [SM](../a-z/sm.md), [TabBar](../a-z/tabbar.md) or [ToolBar](../a-z/toolbar.md), this property specifies the name of, or ref to, a [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md), or [Metafile](../a-z/metafile.md) which is drawn as a *background* on the object. Other controls and graphical objects are drawn on top of this background.


When it refers to a [Metafile](../a-z/metafile.md), the Picture property specifies the name of, or ref to, the [Metafile](../a-z/metafile.md) to be drawn in the object. When it refers to a [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md), the value of the Picture property is a 2-element vector whose elements specify the name of, or ref to, the [Bitmap](../a-z/bitmap.md), or [Icon](../a-z/icon.md), and the manner in which it is displayed. This is specified as an integer as follows:


| 0 | The [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) is drawn in        the top left corner of the object. |
| --- | ---  |
| 1 | The [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) is tiled (replicated) to fill the object. |
| 2 | The [Bitmap](../a-z/bitmap.md) is scaled (up or down) to fit exactly in the object. This setting does not apply to an [Icon](../a-z/icon.md) whose size is fixed. |
| 3 | The [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) is drawn in the centre of the object. This is the default. Note that the centre of the [Bitmap](../a-z/bitmap.md) is positioned over the centre of the object, so that you see the middle portion of a [Bitmap](../a-z/bitmap.md) that is larger than the object in which it is displayed. |



For example, the following statements produce a [Form](../a-z/form.md) filled with the CARS bitmap.
```apl
      'CARS' ⎕WC 'Bitmap' 'C:\WINDOWS\CARS'
      'f1' ⎕WC 'Form' ('Picture' 'CARS' 1)
```



An easy way to provide a customised pushbutton is to create a [Button](../a-z/button.md) whose Picture property specifies the name of, or ref to, a [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md), using drawmode 3 (the default). This causes the corresponding bitmap or icon to be drawn in the centre of the [Button](../a-z/button.md). So long as the [Button](../a-z/button.md) is larger than the bitmap or icon, its borders (which give it its 3-dimensional appearance and "pushbutton" behaviour) will be unaffected.


Note that if Picture is set on a [Button](../a-z/button.md) whose [Style](../a-z/style.md) is `'Radio'` or `'Check'`, the Button assumes pushbutton appearance, although its radio/check behaviour is preserved.


For an [Image](../a-z/image.md) object, the Picture property specifies the name of, or ref to, a [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) or [Metafile](../a-z/metafile.md) object to be drawn, or a vector of names or refs. The [Image](../a-z/image.md) is a graphical object and is drawn *on top of* the background. It does not support the drawmode options provided by the objects in which Picture specifies the background.


For the [Clipboard](../a-z/clipboard.md) object, Picture is a "set-only" property that allows you to place a specified [Bitmap](../a-z/bitmap.md) object into the Windows clipboard. To place a [Metafile](../a-z/metafile.md) object into the clipboard, use its [Metafile](../a-z/metafile.md) property.


