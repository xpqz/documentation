




<h1 class="heading"><span class="name">Picture</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Button](./button.md) [Clipboard](./clipboard.md) [CoolBand](./coolband.md) [Form](./form.md) [Group](./group.md) [Image](./image.md) [MDIClient](./mdiclient.md) [SM](./sm.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) | [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [Clipboard](./clipboard.md) | [CoolBand](./coolband.md) | [Form](./form.md) | [Group](./group.md) | [Image](./image.md) | [MDIClient](./mdiclient.md) | [SM](./sm.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [Clipboard](./clipboard.md) |
| [CoolBand](./coolband.md) | [Form](./form.md) | [Group](./group.md) |
| [Image](./image.md) | [MDIClient](./mdiclient.md) | [SM](./sm.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) |


Description


The Picture property specifies a bitmap, icon, or other image for an object.



For [Button](./button.md), [Form](./form.md), [Group](./group.md), [MDIClient](./mdiclient.md), [Static](./static.md), [StatusBar](./statusbar.md), [StatusField](./statusfield.md), [SubForm](./subform.md), [SM](./sm.md), [TabBar](./tabbar.md) or [ToolBar](./toolbar.md), this property specifies the name of, or ref to, a [Bitmap](./bitmap.md), [Icon](./icon.md), or [Metafile](./metafile.md) which is drawn as a *background* on the object. Other controls and graphical objects are drawn on top of this background.


When it refers to a [Metafile](./metafile.md), the Picture property specifies the name of, or ref to, the [Metafile](./metafile.md) to be drawn in the object. When it refers to a [Bitmap](./bitmap.md) or [Icon](./icon.md), the value of the Picture property is a 2-element vector whose elements specify the name of, or ref to, the [Bitmap](./bitmap.md), or [Icon](./icon.md), and the manner in which it is displayed. This is specified as an integer as follows:

| 0 | The [Bitmap](./bitmap.md) or [Icon](./icon.md) is drawn in        the top left corner of the object. |
| --- | ---  |
| 1 | The [Bitmap](./bitmap.md) or [Icon](./icon.md) is tiled (replicated) to fill the object. |
| 2 | The [Bitmap](./bitmap.md) is scaled (up or down) to fit exactly in the object. This setting does not apply to an [Icon](./icon.md) whose size is fixed. |
| 3 | The [Bitmap](./bitmap.md) or [Icon](./icon.md) is drawn in the centre of the object. This is the default. Note that the centre of the [Bitmap](./bitmap.md) is positioned over the centre of the object, so that you see the middle portion of a [Bitmap](./bitmap.md) that is larger than the object in which it is displayed. |



For example, the following statements produce a [Form](./form.md) filled with the CARS bitmap.
```apl
      'CARS' ⎕WC 'Bitmap' 'C:\WINDOWS\CARS'
      'f1' ⎕WC 'Form' ('Picture' 'CARS' 1)
```



An easy way to provide a customised pushbutton is to create a [Button](./button.md) whose Picture property specifies the name of, or ref to, a [Bitmap](./bitmap.md) or [Icon](./icon.md), using drawmode 3 (the default). This causes the corresponding bitmap or icon to be drawn in the centre of the [Button](./button.md). So long as the [Button](./button.md) is larger than the bitmap or icon, its borders (which give it its 3-dimensional appearance and "pushbutton" behaviour) will be unaffected.


Note that if Picture is set on a [Button](./button.md) whose Style is `'Radio'` or `'Check'`, the Button assumes pushbutton appearance, although its radio/check behaviour is preserved.


For an [Image](./image.md) object, the Picture property specifies the name of, or ref to, a [Bitmap](./bitmap.md), [Icon](./icon.md) or [Metafile](./metafile.md) object to be drawn, or a vector of names or refs. The [Image](./image.md) is a graphical object and is drawn *on top of* the background. It does not support the drawmode options provided by the objects in which Picture specifies the background.


For the [Clipboard](./clipboard.md) object, Picture is a "set-only" property that allows you to place a specified [Bitmap](./bitmap.md) object into the Windows clipboard. To place a [Metafile](./metafile.md) object into the clipboard, use its [Metafile](./metafile.md) property.


