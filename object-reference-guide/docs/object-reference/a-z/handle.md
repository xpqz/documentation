




<h1 class="heading"><span class="name">Handle</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBar](./coolbar.md) [Cursor](./cursor.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Font](./font.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Icon](./icon.md) [ImageList](./imagelist.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [Menu](./menu.md) [MenuBar](./menubar.md) [Metafile](./metafile.md) [OLEClient](./oleclient.md) [OLEServer](./oleserver.md) [Printer](./printer.md) [ProgressBar](./progressbar.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) | [Cursor](./cursor.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Icon](./icon.md) | [ImageList](./imagelist.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [MenuBar](./menubar.md) | [Metafile](./metafile.md) | [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) |
| [Cursor](./cursor.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Icon](./icon.md) | [ImageList](./imagelist.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [MenuBar](./menubar.md) |
| [Metafile](./metafile.md) | [OLEClient](./oleclient.md) | [OLEServer](./oleserver.md) |
| [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [PropertySheet](./propertysheet.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) |
| [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) |
| [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


This is a read-only property that reports the *handle* associated with an object. For a visual object, such as a [Form](./form.md) or a [Button](./button.md), this is the window handle. For a [Printer](./printer.md), it is the *printer device context*.


This handle allows you to access the corresponding object directly with Windows API functions via `⎕NA`. This facility must be used with care and the responsibility for its behaviour is entirely yours. Do NOT use it to delete an object. This will cause APL to crash.


An example of the use of the Handle property is to set tab stops in a [List](./list.md) object. This is illustrated by the following function:
```apl
     ∇ obj TABSTOPS stops;I;LB_SETTABSTOPS;SetTabStops;sink;args
[1]   ⍝ Sets the tabstops in the List Box OBJ to be at
[2]   ⍝ stops Horizontal Dialog units.
[3]   ⍝ Sends LB_SETTABSTOPS (402) to the List Box
[4]   ⍝ See Windows SDK for Details.
[5]
[6]    I←obj ⎕WG'Items'
[7]
[8]    LB_SETTABSTOPS←402
[9]    'SetTabStops'⎕NA'U4 USER32|SendMessageA U4 U4 U4 <U4[]'
[10]
[11]   args←(obj ⎕WG'Handle') LB_SETTABSTOPS (⍴,stops)(,stops)
[12]   sink←SetTabStops args
[13]
[14]   obj ⎕WS'Items'I
     ∇
```



