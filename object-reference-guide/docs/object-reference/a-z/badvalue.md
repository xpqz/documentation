




<h1 class="heading"><span class="name">BadValue</span></h1>

Applies To: [ButtonEdit](./buttonedit.md) [Edit](./edit.md) [Spinner](./spinner.md)


**Description**


If enabled, this event is reported by an [Edit](./edit.md) or [Spinner](./spinner.md) object  when the user enters invalid data into the object and then switches focus to another control or to another application.  Data is invalid if it conflicts with the [FieldType](./fieldtype.md) property, or for a [Spinner](./spinner.md) if it is outside the range specified by the [Limits](./limits.md) property.


The default action of the event is to sound the bell (beep). You can disable this action by returning 0 from a callback function or by setting its action code to `¯1`. Note that in neither case is the [Value](./value.md) property of the object updated. The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'BadValue'` or 180 |
| `[3]` | Object name | character vector |


The third element of the event message is either the name of the control to which the user has switched the focus, or is an empty vector if the focus has gone to another application.



