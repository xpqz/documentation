




<h1 class="heading"><span class="name">Locator</span></h1>

| [Parents](../ParentLists/Locator.htm) | [Children](../ChildLists/Locator.htm) | [Properties](../PropLists/Locator.htm) | [Methods](../MethodLists/Locator.htm) | [Events](../EventLists/Locator.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | Allows the user to input a point, ellipse, line or rectangle. |
| --- | ---  |


**Description**


This object is used to obtain graphical input from the user. Like a pop-up
menu or a [MsgBox](../a-z/msgbox.md), the Locator is a *modal* object whose interaction with the user is initiated by a "local" [`⎕DQ`](../../Language/System%20Functions/dq.htm).



This is terminated when the user releases a mouse button or presses any key
other than a cursor movement key, Shift, Ctrl or Alt. It is usual to initiate
the [`⎕DQ`](../../Language/System%20Functions/dq.htm) for the Locator from within a callback function attached to a [MouseDown](../a-z/mousedown.md) (1) [Event](../a-z/event.md).


When the "local" [`⎕DQ`](../../Language/System%20Functions/dq.htm) is terminated, a [Locator](../a-z/locator.md) (80) [Event](../a-z/event.md) is generated. The associated event message contains the new position and size of
the Locator, together with how the event was generated (keystroke or mouse
button). To obtain the Locator's new position or size, you **must** enable
the event by setting its "action" code to 1, or to the name of a
suitable callback function.


The value of the [Style](../a-z/style.md) property determines
the type of locator displayed. It may be `'Point'`,
`'Line'`, `'Rect'`,
or `'Ellipse'`. The default value is `'Rect'`.
The value of the [Sizeable](../a-z/sizeable.md) property is 0 or
1 and determines whether or not "rubberbanding" is enabled. Its
default value is 1 which turns "rubberbanding" on. The [Size](../a-z/size.md) property determines the initial size of the Locator when displayed by [`⎕DQ`](../../Language/System%20Functions/dq.htm).
Its default value is (0,0).


If [Style](../a-z/style.md) is `'Rect'` the Locator displays a rectangle. One corner of the rectangle is positioned at [Posn](../a-z/posn.md).
The diagonally opposite corner is positioned at ([Posn](../a-z/posn.md)+[Size](../a-z/size.md)).
If [Sizeable](../a-z/sizeable.md) is 0, the entire rectangle is
dragged as the mouse is moved. If [Sizeable](../a-z/sizeable.md) is 1, the


corner initially defined by ([Posn](../a-z/posn.md)+[Size](../a-z/size.md))
is dragged (rubberbanding the rectangle) as the mouse is moved. The rectangle
disappears when the operation is terminated. The new position or size of the
rectangle is reported in the [Locator](../a-z/locator.md) event
message.


If [Style](../a-z/style.md) is `'Ellipse'` the Locator displays an ellipse. One corner of the bounding rectangle of the
ellipse is positioned at [Posn](../a-z/posn.md). The diagonally
opposite corner is positioned at ([Posn](../a-z/posn.md)+[Size](../a-z/size.md)).
If [Sizeable](../a-z/sizeable.md) is 0, the entire ellipse is
dragged as the mouse is moved. If [Sizeable](../a-z/sizeable.md) is 1, the corner of the bounding rectangle initially defined by ([Posn](../a-z/posn.md)+[Size](../a-z/size.md))
is dragged (rubberbanding the ellipse) as the mouse is moved. The ellipse
disappears when the operation is terminated. The new position or size of the
bounding rectangle of the ellipse is reported in the [Locator](../a-z/locator.md) event message.


If [Style](../a-z/style.md) is `'Line'` the Locator displays a line drawn between the points defined by [Posn](../a-z/posn.md) and [Posn](../a-z/posn.md)+[Size](../a-z/size.md).
If [Sizeable](../a-z/sizeable.md) is 0, the line is dragged with
the cursor as the mouse is moved. If [Sizeable](../a-z/sizeable.md) is 1, the end of the line initially defined by [Posn](../a-z/posn.md)+[Size](../a-z/size.md) is dragged (rubberbanding the line) as the mouse is moved. The line disappears
when the operation is terminated. The new position or size of the line is
reported in the [Locator](../a-z/locator.md) event message.


If `'Style'` is `'Point'`,
the values of [Sizeable](../a-z/sizeable.md) and [Size](../a-z/size.md) are ignored. During the [`⎕DQ`](../../Language/System%20Functions/dq.htm) no visible feedback (other than the cursor) is provided as the user moves the
mouse. When the [`⎕DQ`](../../Language/System%20Functions/dq.htm) terminates, the new position of the Locator is reported in the [Locator](../a-z/locator.md) event message.


The [Step](../a-z/step.md) property is a 2-element integer vector (default value 1 1) that
specifies the increments (in pixels) by which the size or position of the
Locator changes in the Y and X directions respectively as the user moves the
Locator.


The Locator is normally initiated from a [MouseDown](../a-z/mousedown.md) (1) event, and it is natural to place it at the current cursor position.
However, if you are using rubberbanding, you will normally want to have the
cursor appear at the end or corner of the Locator that moves. If you start with a non-zero sized Locator, you must set [Posn](../a-z/posn.md) (which defines the **fixed** end or corner) to the current cursor position
minus [Size](../a-z/size.md) to achieve this effect.


