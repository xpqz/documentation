




<h1 class="heading"><span class="name">FireOnce</span></h1>

| Applies To: | [Timer](../a-z/timer.md) |
| --- | ---  |


**Description**


This property specifies one-off  behaviour for a [Timer](../a-z/timer.md) object. It has the value 0, 1 or 2.


Setting FireOnce to 1, will cause the [Timer](../a-z/timer.md) to generate a single event and no more unless it is reset. After generating the single event, FireOnce is automatically set to 2 and this change occurs prior to the invocation of a callback function.


Setting FireOnce to 2 will cause the [Timer](../a-z/timer.md) to behave as if it has already raised its single event.


FireOnce honours the value of the [Active](../a-z/active.md) property but does not change it. So setting FireOnce to 1 when [Active](../a-z/active.md) is 0 will not immediately cause an event. If [Active](../a-z/active.md) is subsequently set to 1, the single [Timer](../a-z/timer.md) event will then occur.



