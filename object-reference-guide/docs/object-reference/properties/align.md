




<h1 class="heading"><span class="name">Align</span></h1>

Applies To

| Applies To: | [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [ListView](../a-z/listview.md) [Menu](../a-z/menu.md) [MenuItem](../a-z/menuitem.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [Splitter](../a-z/splitter.md) [StatusBar](../a-z/statusbar.md) [TabBar](../a-z/tabbar.md) [TabBtn](../a-z/tabbtn.md) [TabControl](../a-z/tabcontrol.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Splitter](../a-z/splitter.md) | [StatusBar](../a-z/statusbar.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) | [TabControl](../a-z/tabcontrol.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) |
| --- | --- | ---  |
| [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) |
| [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Splitter](../a-z/splitter.md) |
| [StatusBar](../a-z/statusbar.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) |
| [TabControl](../a-z/tabcontrol.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) |


Description


For an [Animation](../a-z/animation.md), the Align property may be `'None'` or `'Centre'` (`'Center'`). If Align is `'None'`, the [Animation](../a-z/animation.md) window is automatically resized to fit the AVI being played. If Align is `'Centre'`, the AVI is centred in the [Animation](../a-z/animation.md) window. If the window is too small, the AVI is clipped.



For a [Button](../a-z/button.md), [Menu](../a-z/menu.md), or [MenuItem](../a-z/menuitem.md) the Align property may be `'None'`, `'Left'` or `'Right'`. If the [Button](../a-z/button.md) Style is `'Radio'` or `'Check'` this property specifies the position of the text relative to the button symbol. The default is `'Right'`. For a [Button](../a-z/button.md) with Style `'Push'`, the value of Align is `'None'`.


For a [Button](../a-z/button.md) with Style `'Radio'` or `'Check'` that is created as a child of a Grid the value of the Align property may also be `'Centre'`or`'Center'.`Either of these values causes the symbol part of the [Button](../a-z/button.md) (the circle or checkbox) to be centred within the corresponding Grid cell(s).


For a [DateTimePicker](../a-z/datetimepicker.md), the Align property specifies the horizontal alignment of the drop-down Calendar which may be `'Left'` (the default) or `'Right'`. This applies only if the Style of the DateTimePicker is `'Combo'`.


For a single-line [Edit](../a-z/edit.md), Align specifies the vertical alignment of the text. It may be `'None'` (the default), `'Centre'` or `'Center'`.


For a [Menu](../a-z/menu.md), [MenuItem](../a-z/menuitem.md), or [StatusField](../a-z/statusfield.md), Align `'Right'` is used to position the object at the right end of its parent [MenuBar](../a-z/menubar.md) or [StatusBar](../a-z/statusbar.md). `'None'` is equivalent to `'Left'` which is the default.


For objects of type [CoolBar](../a-z/coolbar.md), [Splitter](../a-z/splitter.md), [Scroll](../a-z/scroll.md), [StatusBar](../a-z/statusbar.md), [TabBar](../a-z/tabbar.md), [ToolBar](../a-z/toolbar.md) and [ToolControl](../a-z/toolcontrol.md), Align may be `'None'`, `'Top'`, `'Bottom'`, `'Left'` or `'Right'`. It specifies to which (if any) of the four sides of the parent the object is anchored and also the default position and size of the object. Specifying Align typically causes the [Attach](../a-z/attach.md) property to be set to appropriate values as follows :

| `Align` | `Attach` |
| --- | ---  |
| `'Top'` | `'Top' 'Left' 'Top' 'Right'` |
| `'Bottom'` | `'Bottom' 'Left' 'Bottom' 'Right'` |
| `'Left'` | `'Top' 'Left' 'Bottom' 'Left'` |
| `'Right'` | `'Top' 'Right' 'Bottom' 'Right'` |


These settings cause the object to remain at a fixed distance (in pixels) from the corresponding edge of the parent. Furthermore, the object will have a fixed height or width, but its length will stretch and shrink as the [Form](../a-z/form.md) is resized.


Note that this does not apply to a [TabControl](../a-z/tabcontrol.md) for which the default value of Attach is `'None'  'None'  'None'  'None'`, regardless of the value of Align.


The default value of Align is `'Right'` for a vertical [Scroll](../a-z/scroll.md), `'Bottom'` for a horizontal [Scroll](../a-z/scroll.md), and `'Top'` for a [CoolBar](../a-z/coolbar.md), [TabBar](../a-z/tabbar.md), [TabControl](../a-z/tabcontrol.md), [ToolBar](../a-z/toolbar.md) and [ToolControl](../a-z/toolcontrol.md). Furthermore, unless [Posn](../a-z/posn.md) and [Size](../a-z/size.md) are specified explicitly, the object is placed along the corresponding edge of its parent.


For a [Scroll](../a-z/scroll.md) object, Align also determines the direction of a [Scroll](../a-z/scroll.md) object unless it is overridden by setting [HScroll](../a-z/hscroll.md) or [VScroll](../a-z/vscroll.md) directly. If neither [HScroll](../a-z/hscroll.md) or VScroll is defined and Align is `'Top'` or `'Bottom'`, a horizontal scrollbar is provided. If neither [HScroll](../a-z/hscroll.md) or [VScroll](../a-z/vscroll.md) is defined and Align is `'None'`, `'Left'` or `'Right'`, a vertical scrollbar is provided.

#### Note


The value of the Align property may only be assigned by `⎕WC` and may not be changed using `⎕WS`.


