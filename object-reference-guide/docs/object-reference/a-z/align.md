




<h1 class="heading"><span class="name">Align</span></h1>

Applies To

| Applies To: | [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [ListView](./listview.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [StatusBar](./statusbar.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [ListView](./listview.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [StatusBar](./statusbar.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) |
| --- | --- | ---  |
| [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [ListView](./listview.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) |
| [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) |
| [StatusBar](./statusbar.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) |


Description


For an [Animation](./animation.md), the Align property may be `'None'` or `'Centre'` (`'Center'`). If Align is `'None'`, the [Animation](./animation.md) window is automatically resized to fit the AVI being played. If Align is `'Centre'`, the AVI is centred in the [Animation](./animation.md) window. If the window is too small, the AVI is clipped.



For a [Button](./button.md), [Menu](./menu.md), or [MenuItem](./menuitem.md) the Align property may be `'None'`, `'Left'` or `'Right'`. If the [Button](./button.md) Style is `'Radio'` or `'Check'` this property specifies the position of the text relative to the button symbol. The default is `'Right'`. For a [Button](./button.md) with Style `'Push'`, the value of Align is `'None'`.


For a [Button](./button.md) with Style `'Radio'` or `'Check'` that is created as a child of a Grid the value of the Align property may also be `'Centre'`or`'Center'.`Either of these values causes the symbol part of the [Button](./button.md) (the circle or checkbox) to be centred within the corresponding Grid cell(s).


For a [DateTimePicker](./datetimepicker.md), the Align property specifies the horizontal alignment of the drop-down Calendar which may be `'Left'` (the default) or `'Right'`. This applies only if the Style of the DateTimePicker is `'Combo'`.


For a single-line [Edit](./edit.md), Align specifies the vertical alignment of the text. It may be `'None'` (the default), `'Centre'` or `'Center'`.


For a [Menu](./menu.md), [MenuItem](./menuitem.md), or [StatusField](./statusfield.md), Align `'Right'` is used to position the object at the right end of its parent [MenuBar](./menubar.md) or [StatusBar](./statusbar.md). `'None'` is equivalent to `'Left'` which is the default.


For objects of type [CoolBar](./coolbar.md), [Splitter](./splitter.md), [Scroll](./scroll.md), [StatusBar](./statusbar.md), [TabBar](./tabbar.md), [ToolBar](./toolbar.md) and [ToolControl](./toolcontrol.md), Align may be `'None'`, `'Top'`, `'Bottom'`, `'Left'` or `'Right'`. It specifies to which (if any) of the four sides of the parent the object is anchored and also the default position and size of the object. Specifying Align typically causes the Attach property to be set to appropriate values as follows :

| `Align` | `Attach` |
| --- | ---  |
| `'Top'` | `'Top' 'Left' 'Top' 'Right'` |
| `'Bottom'` | `'Bottom' 'Left' 'Bottom' 'Right'` |
| `'Left'` | `'Top' 'Left' 'Bottom' 'Left'` |
| `'Right'` | `'Top' 'Right' 'Bottom' 'Right'` |


These settings cause the object to remain at a fixed distance (in pixels) from the corresponding edge of the parent. Furthermore, the object will have a fixed height or width, but its length will stretch and shrink as the [Form](./form.md) is resized.


Note that this does not apply to a [TabControl](./tabcontrol.md) for which the default value of Attach is `'None'  'None'  'None'  'None'`, regardless of the value of Align.


The default value of Align is `'Right'` for a vertical [Scroll](./scroll.md), `'Bottom'` for a horizontal [Scroll](./scroll.md), and `'Top'` for a [CoolBar](./coolbar.md), [TabBar](./tabbar.md), [TabControl](./tabcontrol.md), [ToolBar](./toolbar.md) and [ToolControl](./toolcontrol.md). Furthermore, unless Posn and Size are specified explicitly, the object is placed along the corresponding edge of its parent.


For a [Scroll](./scroll.md) object, Align also determines the direction of a [Scroll](./scroll.md) object unless it is overridden by setting HScroll or VScroll directly. If neither HScroll or VScroll is defined and Align is `'Top'` or `'Bottom'`, a horizontal scrollbar is provided. If neither HScroll or VScroll is defined and Align is `'None'`, `'Left'` or `'Right'`, a vertical scrollbar is provided.

#### Note


The value of the Align property may only be assigned by `⎕WC` and may not be changed using `⎕WS`.


