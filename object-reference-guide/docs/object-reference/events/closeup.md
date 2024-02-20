




<h1 class="heading"><span class="name">CloseUp</span></h1>

Applies To: [DateTimePicker](../a-z/datetimepicker.md)


**Description**


If enabled, this event is reported by a [DateTimePicker](../a-z/datetimepicker.md) object just before the drop-down calendar is hidden. It applies only if the Style of the [DateTimePicker](../a-z/datetimepicker.md) is `'Combo'`.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'CloseUp'` or 46 |


This event is reported for information only and cannot be disabled or modified in any way.



