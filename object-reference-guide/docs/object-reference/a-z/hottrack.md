




<h1 class="heading"><span class="name">HotTrack</span></h1>
| Applies To: | [TabControl](./tabcontrol.md) |
| --- | ---  |

| Applies To: | [TabControl](./tabcontrol.md) | [TabControl](./tabcontrol.md) |  |  |
| --- | --- | ---  |
| [TabControl](./tabcontrol.md) |  |  |


Description


The HotTrack property specifies whether or not the tabs or buttons in a [TabControl](./tabcontrol.md) object ( which are represented by [TabButton](./tabbutton.md) objects), are automatically highlighted by the mouse pointer.


HotTrack is a single number with the value 0 (no highlighting) or 1. The default is 0.


If HotTrack is 1 and the Style property of the [TabControl](./tabcontrol.md) is `'Tabs'` or `'Buttons'`, the text defined by the Caption property of the [TabButton](./tabbutton.md) is highlighted when the mouse pointer is placed over the tab or button. If Style is `'FlatButtons'`, the button is highlighted by being *raised*.


The value of HotTrack is effective only when the object is created with `⎕WC`.



