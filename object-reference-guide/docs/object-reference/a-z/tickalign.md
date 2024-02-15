




<h1 class="heading"><span class="name">TickAlign</span></h1>

| Applies To: | [TrackBar](./trackbar.md) |
| --- | ---  |


**Description**


TickAlign determines the position of the tick marks in a [TrackBar](./trackbar.md) object. For a horizontal [TrackBar](./trackbar.md), TickAlign may be either `'Bottom'` (the default), `'Top'` or `'Both'`. If TickAlign is `'Bottom'`, the ticks are drawn *below* the slider. If TickAlign is `'Top'`, the ticks are drawn above it. If TickAlign is `'Both'`, the ticks are drawn above and below.


For a vertical [TrackBar](./trackbar.md), TickAlign may be either `'Right'` (the default), `'Left'`, or `'Both'` and similarly specifies to which side of the slider bar the ticks are drawn. Note that TickAlign may only be set when the TrackBar is created with `⎕WC` and may not subsequently be altered using `⎕WS`.


Note that ticks are not drawn if the value of [HasTicks](hasticks.md) is 0



