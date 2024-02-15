




<h1 class="heading"><span class="name">Configure</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) |
| [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) |
| [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) |
| [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) |
| [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) |
| [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |


Description


If enabled, this event is generated when the configuration of an object
(position and/or size) is about to change.



For a [Form](../a-z/form.md), the event is generated when the [Form](../a-z/form.md) is resized or moved by the user.


For any object other than a [Form](../a-z/form.md), it can
occur in one of two ways. Firstly, whenever a [Form](../a-z/form.md) is resized, the system (by default) re-arranges its children so as to maintain
their relative position and size. This generates a Configure event (if enabled)
for each one of them.


Secondly, it can occur as a result of the user resizing the object directly.
This facility is enabled by setting the object's [Sizeable](../a-z/sizeable.md) property to 1.


Note that a Configure event is not reported when an object is moved
using "drag & drop". See [Dragable](../a-z/dragable.md) (property) and [DragDrop](../a-z/dragdrop.md) (event) for details
of this operation.



The event message reported as the result of `⎕DQ`,
or supplied as the right argument to your callback function, is a 6-element
vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Configure'` or 31 |
| `[3]` | Y | y-position of top left corner |
| `[4]` | X | x-position of top left corner |
| `[5]` | H | height of object |
| `[6]` | W | width of object |



For any object, the operation can be prevented by returning a scalar 0 from
the callback function associated with the Configure event.

#### Full-Drag Considerations


The user may choose a system option, described here as *full-drag*,
whereby the contents of the window are re-arranged during a resize operation.


If you manage the geometry of your controls using the Attach property, APL
honours *full drag* during resize, changing the size and position of your
controls dynamically for you.


However, if you manage the geometry of controls using Configure event
callbacks, you should consider the following.

1. If full drag is in enabled, APL generates Configure events *during* the resize operation, allowing you to dynamically alter the geometry of
    controls as you wish. However, the following restrictions apply:
2. Configure callbacks will only be executed when the interpreter is *idle*.
    For example during a `⎕DQ` or
    during Session input (6-space prompt). If the user attempts to move/resize a
    window that has Configure callbacks attached when the interpreter is busy,
    the move/resize is not started. This is similar to the operation in non *full
    drag* mode, where the move/resize is allowed but the callback does not
    execute until the interpreter again becomes idle.
3. The callback cannot be traced. It is necessary to debug the callback code
    with *full drag* disabled.
4. Any untrapped errors in the Configure callback will not halt execution in
    the normal way, but will instead be reported in the *Status Window*.
    Note that it is also not possible to trap such errors higher up the SI stack
    than the Configure Callback.
5. There are some programming styles to be avoided if *full drag* Configure callbacks are to be processed correctly. For example events
    generated by monadic `⎕NQ` within
    a Configure callback will not be processed until the entire resize operation
    has been completed.
6. It is not possible to save a workspace from within a Configure Callback in
    *full drag* mode.

The above restrictions apply to Configure events when *full drag* is
enabled, but *only* when *full drag* is enabled. The behaviour of
Configure callbacks with *full drag* disabled is the same as for other
events.


