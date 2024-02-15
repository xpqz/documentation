




<h1 class="heading"><span class="name">ThumbDrag</span></h1>
| Applies To: | [Scroll](../a-z/scroll.md) | [TrackBar](../a-z/trackbar.md) |
| --- | --- | ---  |

| Applies To: | [Scroll](../a-z/scroll.md) [TrackBar](../a-z/trackbar.md) | [Scroll](../a-z/scroll.md) | [TrackBar](../a-z/trackbar.md) |  |
| --- | --- | ---  |
| [Scroll](../a-z/scroll.md) | [TrackBar](../a-z/trackbar.md) |  |


Description


If enabled, this event is generated when the user drags the thumb in a [TrackBar](../a-z/trackbar.md) object. The event is reported *after* the value of the Thumb property has been updated and is reported continuously as the thumb is dragged. You may not disable this event or alter its effect with a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'ThumbDrag'` or 440 |
| `[3]` | Thumb value | Integer. The new value of the Thumb property resulting from the user dragging the thumb. |



