



<h1 class="heading"><span class="name">Change</span></h1>

Applies To: [ButtonEdit](./buttonedit.md) [Combo](./combo.md) [Edit](./edit.md) [RichEdit](./richedit.md) [Spinner](./spinner.md)


**Description**


If enabled, this event is reported when the user alters the text in a [Combo](./combo.md) or [Edit](./edit.md) object (by typing). The event is not applicable for a [Combo](./combo.md) with [Style](./style.md)`'Drop'` because this [Style](./style.md) does not allow the user to alter data. The Change event is not reported repeatedly as the user edits the data. Instead, it is reported when the user indicates that he has finished with the field by :

1. clicking on another object, **or**
2. causing an event on another object (without altering the input focus) which will fire a callback function or cause [`⎕DQ`](../../Language/System Functions/dq.htm) to terminate. This can occur if the user chooses a [MenuItem](./menuitem.md), or fires a [Button](./button.md) with the [Default](./default.md) or [Cancel](./cancel.md) property by pressing Enter or Esc, or selects an object using an accelerator key.

The purpose of the Change event is to allow the application to validate data which has been newly entered to the field, before proceeding with another action. It is for this reason that the event is fired not just when the input focus changes, but also when the user takes some action that could cause the application to do something else.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Change'` or 36 |
| `[3]` | Object name | character vector (name of object that is to receive the focus or generate an event) |


If the focus is transferred to an external application, the third element is an empty vector.


The default processing for this event is to allow the focus to change (if applicable) and to reset the internal flag that indicates that the data in the field has changed.


If you disable the event by setting the "action" code to `¯1`, or inhibit it by returning 0 from a callback, the focus change (if applicable) is allowed to proceed, but the internal flag is not reset. If you wish to prevent the focus change you must explicitly reset the focus back onto the object that generated the event.


If the event was generated because the user switched to another application, and you return a 0 from your callback (because the data was not valid), the flag marking the [Combo](./combo.md) or [Edit](./edit.md) as having been changed remains set. If the user returns to your application by re-focusing on the same [Combo](./combo.md) or [Edit](./edit.md), nothing happens immediately, but because the field is marked as changed (the flag was not reset) you will get another Change event when he leaves it. However, if the user returns to your application in some other way, e.g. by focusing on another object or by selecting a [MenuItem](./menuitem.md), a second Change event will be generated immediately.


The following function illustrates how Change events can be processed. The `Check` function referred to in line[4] is assumed to return 1 if the data is valid and 0 if not.
```apl
[0]   R←VALIDATE Msg
[1]  ⍝ Validates field contents after Change event
[2]
[3]  ⍝ Normal exit (R←1) if data is valid
[4]    →(R←Check⊃Msg)/Exit
[5]
[6]  ⍝ R now 0, so field remains marked as "changed"
[7]
[8]  ⍝ If user has switched to another application,
[9]  ⍝ we need take no further action because we will
[10] ⍝ get a second Change event when he returns.
[11]  →(''≡3⊃Msg)/Exit
[12]
[13] ⍝ Display error box (prepared earlier)
[14]   'ERR' ⎕WS 'Text' 'Data is invalid'
[15]   ⎕DQ'ERR'
[16]
[17] ⍝ Restore focus to bad field
[18]   ⎕NQ(⊃Msg)40
[19]
[20] Exit:
```


