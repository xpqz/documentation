




<h1 class="heading"><span class="name">SplitObj1</span></h1>
| Applies To: | [Splitter](./splitter.md) |
| --- | ---  |

| Applies To: | [Splitter](./splitter.md) | [Splitter](./splitter.md) |  |  |
| --- | --- | ---  |
| [Splitter](./splitter.md) |  |  |


Description


The SplitObj1 property specifies the name of, or ref to, one of up to two objects managed by a [Splitter](./splitter.md) object. The object must be one of the following types:


If the [Style](style.md) property of the [Splitter](./splitter.md) is `'Vert'`, the object specified by SplitObj1 is positioned at (0 0) and sized to occupy the space in its parent to the left of the [Splitter](./splitter.md), with the [Splitter](./splitter.md) itself attached to its right edge.


If the [Style](style.md) property of the [Splitter](./splitter.md) is `'Horz'`, the object specified by SplitObj1 is positioned at (0 0) and sized to occupy the space in its parent above the [Splitter](./splitter.md), with the [Splitter](./splitter.md) itself attached to its bottom edge.


If SplitObj1 is empty, the [Splitter](./splitter.md) manages the single object specified by SplitObj2 and the space to the left or above the [Splitter](./splitter.md) is empty or controlled by another [Splitter](./splitter.md).


| Button | Calendar | Combo | Edit | Grid | Group |
| --- | --- | --- | --- | --- | ---  |
| Label | List | ListView | MDIClient | ProgressBar | RichEdit |
| Scroll | Spinner | Static | StatusBar | SubForm | TabBar |
| TabControl | ToolBar | TrackBar | TreeView | UpDown |  |


