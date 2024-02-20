




<h1 class="heading"><span class="name">GestureRotate</span></h1>

**Applies To**


**Description**


This event is reported when the user touches  two fingers on an object and twists them clockwise or anticlockwise.




The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 5-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GestureRotate'` or 495 |
| `[3]` | Flags | integer which reports the state of the gesture |
| `[4]` | Location | 2-element integer vector containing the y and x-position respectively of the  point midway between the two fingers. These are reported in pixel coordinates relative to the origin of the screen. |
| `[5]` | Angle | a scalar number which represents the angle of rotation of the twist measured in radians `(0 → ○2` ) from the x-axis in a counter-clockwise direction. |




The Flags parameter [3] which reports the state of the Gesture, is an integer with the value 0, 1 (**GF_BEGIN**),or 4 (**GF_END**) with the following meanings:


| Name | Value | Description |
| --- | --- | ---  |
| `` | 0 | A gesture is in progress |
| `GF_BEGIN` | 1 | A gesture is starting. |
| `GF_END` | 4 | A gesture has finished. |



When the user first touches two fingers on an object and begins to twist, the object generates a GestureRotate event with a `Flags` parameter of 1 (`GF_BEGIN`). As the user continues to twist his fingers, the object generates a series of GestureRotate events with a `Flags` parameter of 0. When the user lifts one or both fingers away, the object generates a final GestureRotate event, with a `Flags` parameter of 4 (`GF_END`).


No other event will be reported between the start and end of a series of GestureRotate events.


Returning zero from the callback disables any default handling by the operating system.


The associated callback is run **immediately** while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback Functions[High-Priority Callback Functions](../../InterfaceGuide/Introduction/High Priority Callbacks.htm#High-Priority_Callback_Functions).


