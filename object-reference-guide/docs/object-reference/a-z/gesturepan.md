




<h1 class="heading"><span class="name">GesturePan</span></h1>

**Applies To**


**Description**


This event is reported when the user touches one or two fingers on an object and drags them .




The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 5-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GesturePan'` or 494 |
| `[3]` | Flags | integer which reports the state of the gesture |
| `[4]` | Location | 2-element integer vector containing the y and x-position respectively of the point at which the gesture applies. These are reported in pixel coordinates relative to the origin (top-left corner) of the object reporting the event. |
| `[5]` | Distance | 2-element integer vector containing the high and low parts (words) of a 64-bit integer that indicates the distance between the two fingers. This will be (0 0) if only one finger is used. |




The Flags parameter [3] which reports the state of the Gesture, is an integer with the value 0, 1 (**GF_BEGIN**), 2 (GF_INERTIA), 4 (**GF_END**) or 6 (**GF_END**+**GF_INERTIA**) with the following meanings:


| Name | Value | Description |
| --- | --- | ---  |
| `` | 0 | A gesture is in progress |
| `GF_BEGIN` | 1 | A gesture is starting. |
| `GF_INERTIA` | 2 | A gesture has triggered inertia. |
| `GF_END` | 4 | A gesture has finished. |



The term **inertia** refers to built-in Windows processing which provides a standardised user-interface including smooth acceleration and de-acceleration of an object.


When the user first touches  an object and begins to drag his finger(s), the object generates a GesturePan event with a `Flags` parameter of 1 (`GF_BEGIN`). Subsequently, if the user drags the object steadily it generates a series of GesturePan events with a `Flags` parameter of 0.  When the user lifts his finger(s) away, the object generates a final GesturePan event, with a `Flags` parameter of 4 (`GF_END`).


If  the user *flicks* an object, the system typically continues to generate GesturePan events after the user has ceased to touch the object. These events are generated in response to the acceleration and deceleration imparted by the *flick*, and the `Flags` parameter for these generated events will be 2 (`GF_INERTIA`) followed (for the last GesturePan event) by 6 (`GF_END`+`GF_INERTIA`).


No other event will be reported between the start and end of a series of GesturePan events.


Returning zero from the callback disables any default handling by the operating system.


The associated callback is run **immediately** while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback Functions[High-Priority Callback Functions](../../InterfaceGuide/Introduction/High Priority Callbacks.htm#High-Priority_Callback_Functions).


