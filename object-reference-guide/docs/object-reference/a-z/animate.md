




<h1 class="heading"><span class="name">Animate</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) |
| [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) |
| [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) |
| [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) |
| [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


The Animate method enables you to produce special effects when showing or hiding objects. There are three types of animation: roll, slide, and alpha-blended fade.




The argument to Animate is a 1 or 2-element array as follows:

| `[1]` | Effects | integer |
| --- | --- | ---  |
| `[2]` | Play time | integer |




The value of the *Effects* parameter is the sum of the following flags:

| Flag | Value | Description |
| --- | --- | ---  |
| AW_HOR_POSITIVE | 1 | Animates the window from left to right. This flag can be used with roll or slide animation. It is ignored when used with the AW_CENTER flag. |
| AW_HOR_NEGATIVE | 2 | Animates the window from right to left. This flag can be used with roll or slide animation. It is ignored when used with the AW_CENTER flag. |
| AW_VER_POSITIVE | 4 | Animates the window from top to bottom. This flag can be used with roll or slide animation. It is ignored when used with the AW_CENTER flag. |
| AW_VER_NEGATIVE | 8 | Animates the window from bottom to top. This flag can be used with roll or slide animation. It is ignored when used with the AW_CENTER flag. |
| AW_CENTER | 16 | Makes the window appear to collapse inward if being hidden or expand outward if being displayed |
| AW_SLIDE | 262144 | Uses slide animation. By default, roll animation is used. This flag is meaningless on its own but is ignored when used with the AW_CENTER flag. |
| AW_BLEND | 524288 | Uses a fade effect. This flag can be used only for a Form. |



The Playtime parameter is optional and specifies the length of time over which the animation is played in milliseconds. The default value depends upon the animation but is typically 200 milliseconds.


