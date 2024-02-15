




<h1 class="heading"><span class="name">SplitObj2</span></h1>

| Applies To: | [Splitter](./splitter.md) |
| --- | ---  |


**Description**


The SplitObj2 property specifies the name of, or ref to, one of up to two objects managed by a [Splitter](./splitter.md) object. The object must be one of the following types:


If the [Style](style.md) property of the [Splitter](./splitter.md) is `'Vert'`, the object specified by SplitObj2 is initially positioned at (0 x), where x is half the width of the parent plus the Size of the [Splitter](./splitter.md), and sized to occupy the space in its parent to the right of the [Splitter](./splitter.md), with the [Splitter](./splitter.md) itself attached to its left edge.


If the [Style](style.md) property of the [Splitter](./splitter.md) is `'Horz'`, the object specified by SplitObj2 is initially positioned at (y 0), where y is half the height of the parent plus the Size of the [Splitter](./splitter.md), and sized to occupy the space in its parent below the [Splitter](./splitter.md), with the [Splitter](./splitter.md) itself attached to its top edge.


If SplitObj2 is empty, the [Splitter](./splitter.md) manages the single object specified by [SplitObj1](splitobj1.md) and the space to the right or below the [Splitter](./splitter.md) is empty or controlled by a second [Splitter](./splitter.md).



| Button | Calendar | Combo | Edit | Grid | Group |
| --- | --- | --- | --- | --- | ---  |
| Label | List | ListView | MDIClient | ProgressBar | RichEdit |
| Scroll | Spinner | Static | StatusBar | SubForm | TabBar |
| TabControl | ToolBar | TrackBar | TreeView | UpDown |  |


