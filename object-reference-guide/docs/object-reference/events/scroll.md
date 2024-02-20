




<h1 class="heading"><span class="name">Scroll</span></h1>

Applies To: [Scroll](../a-z/scroll.md) [TrackBar](../a-z/trackbar.md)


**Description**


If enabled, this event is generated when the user attempts to move the thumb in a scrollbar. This can be done in one of three ways:

1. dragging the thumb.
2. clicking in one of the "arrow" buttons situated at the ends of the scrollbar. This is termed a small change, the size of which is defined by [Step](../a-z/step.md)[1].
3. clicking in the body of the scrollbar. This is termed a large change, the size of which is defined by [Step](../a-z/step.md)[2].

The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 4-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Scroll'` or 37 |
| `[3]` | Scroll Type | numeric |
| `[4]` | Position | numeric |


The value of Scroll Type is 0 (drag), 1 or `¯1` (small change) or 2 or `¯2` (large change). The sign indicates the direction.


The value of Position is the new (requested) position of the thumb. Notice however, that the event is generated **before** the thumb is actually moved. If your callback function returns a scalar 0, the position of the thumb will remain unaltered.



